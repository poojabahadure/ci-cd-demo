pipeline {
agent any
tools {
go 'gotest'
}
environment {
GO111MODULE='on'
}
stages {
stage('Test') {
steps {
git 'https://github.com/poojabahadure/ci-cd-demo.git'
sh 'go test ./...'
}
}
stage('Build') {
steps {
git 'https://github.com/poojabahadure/ci-cd-demo.git'
sh 'go build .'
}
}
stage('Run') {
steps {
sh 'cd /var/lib/jenkins/workspace/full-cicd-go1 && go-webapp-sample &'
}
}
}
}
