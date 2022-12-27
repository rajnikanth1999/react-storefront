pipeline {
    agent any
triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('build') {
            steps {
                sh 'docker image build -t praveenrajnikanth/workshop:store ./Dockerfile.base'
            }
        }
        stage('push') {
            steps {
                sh 'docker image push praveenrajnikanth/workshop:store'
            }
        }
    }
}