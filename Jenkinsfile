pipeline {
    agent any

    stages {
        stage('checkout-git') {
            steps {
                git branch: 'main', url: 'https://github.com/vimalkumar-j/demo-counter-app.git'
            }
        }

        stage('unit test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('integration test') {
            steps {
                sh 'mvn verify -DskipUnitTests'
            }
        }      

        stage('Maven build') {
            steps {
                sh 'mvn clean install'
            }
        }                    
    }
}
