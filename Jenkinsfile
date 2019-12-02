pipeline
{
agent any
    stages
    {
stage('Git-Checkout')
{
  steps
  {
echo "Checkout from GitHub!!";
git 'https://github.com/madhavreddy44/Pipeline_Script.git'
}
}
stage('Build'){
  steps{
echo "Building the Project";
bat label: '', script: 'Build.bat'
}
}
stage('Unit-Test'){
  steps{
echo "Running the Junit Test!!";
bat label: '', script: 'Unit.bat'
}
}
stage('Quality-Gate '){
  steps{
echo "QA Verification Going on";
bat label: '', script: 'Quality.bat'
}
}
stage('Deploy'){
  steps{
echo "Deploing on Stage Env ";
bat label: '', script: 'Deploy.bat'


}
}
}

post {
always {
echo 'this will always run'
}

success  {
echo 'this will  run only if sucessful'
}
failure  {
echo 'this will  run only if failed'
}
unstable  {
echo 'this will  run only if unstable'
}
}
}
