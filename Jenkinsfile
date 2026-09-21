pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                bat '"C:\\Users\\hello\\Downloads\\apache-maven-3.9.16-bin\\apache-maven-3.9.16\\bin\\mvn.cmd" clean package'
            }
        }

        stage('Deploy') {
            steps {
                bat 'copy /Y target\\WebApp.war "C:\\Users\\hello\\Downloads\\apache-tomcat-10.1.59-windows-x64\\apache-tomcat-10.1.59\\webapps\\WebApp.war"'
            }
        }
    }
}
