pipeline{

    agent any

    tools{
        maven "maven"
    }

    stages{
        stage("SCM Checkout"){
            steps{
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/AadiDecoder/jenkins-ci-cd.git']])
            }
        }
        stage("build stage"){
            steps{
                sh 'mvn clean install'
            }
        }
    }
}