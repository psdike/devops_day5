pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'rm -rf maven-web/'
                sh 'pwd'
                sh 'git clone https://github.com/psdike/maven-web.git'
                dir ('maven-web'){
                 sh 'pwd'
                 sh 'mvn clean package'
                }
               
                
                
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                dir ('maven-web'){
                 sh 'pwd'
                 sh 'mvn test'
                }
                
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                
               
            }
        }
    }
}
