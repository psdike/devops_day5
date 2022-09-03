pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                git clone 'https://github.com/psdike/maven-web.git'
                cd maven-web
                mvn clean package
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                mvn test
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                cd target/
               
            }
        }
    }
}
