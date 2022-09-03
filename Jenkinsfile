pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'rm -rf maven-web/'
                sh 'pwd'
                sh 'git clone https://github.com/psdike/maven-web.git'
                sh 'cd maven-web'
                sh 'pwd'
                echo '==============$(pwd)=============================='
                
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                
               
            }
        }
    }
}
