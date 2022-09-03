pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'git clone https://github.com/psdike/maven-web.git'
                cd maven-web/
                sh 'mvn clean package'
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
                cd target/
                cp *.war c:\tomcat\webapps\
            }
        }
    }
}
