pipeline {
agent any
stages {
//stage('Clone repository') {
//steps {
//checkout([$class: 'GitSCM',
//branches: [[name: '*/main']],
//userRemoteConfigs: [[url: 'https://github.com/Shreya-Shinde/PES1UG22CS839_jenkins.git']]])
//}
//}
stage('Build') {
steps {
build 'PES1UG22CS839-1'
sh 'g++ main.cpp-o output'
}
}
stage('Test') {
steps {
sh './output'
}
}
stage('Deploy') {
steps {
echo 'deploy'
}
}
}
post{
failure{
error 'Pipeline failed'
}
}
}
