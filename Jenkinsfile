pipeline {
    agent any

    tools {
       maven 'Maven3'
       jdk 'JDK17'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run') {
            steps {
                sh 'java -cp target/java-jenkins-demo-1.0.jar com.example.App'
            }
        }
    }
}
