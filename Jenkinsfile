pipeline{
  agent any
  stages{
    stage('Build'){
steps{
build 'PES1UG21CS693'
sh 'g++ main/hello.cpp -o output'
}
}
stage('Test'){
steps{
sh './output'
}
}
stage('Deploy'){
steps{
echo 'deploy'
}
}
}
post{
failure{
error 'pipline failed'
}
}
}