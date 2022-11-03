pipeline {
    agent any
    stages {
        stage('Github clone') { 
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'githubtoken', url: 'https://github.com/KameshvaranV/Pet-App']]]) 
            }
        }
        stage('Docker Build'){
            steps{
                sh "docker build . "
            }
        }
    }
}
