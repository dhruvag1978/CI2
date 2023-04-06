pipeline {

    agent any 

    stages {

        stage('GIT CHECKOUT') {

            steps {
                git branch: 'main', url: 'https://github.com/dhruvag1978/CI2.git'
            }
        }
        stage('UNIT TESTING') {
            steps {
                sh 'mvn test'
            }
        }
        stage('INTEGRATION TESTING') {
            steps {
                sh 'mvn verify -DskipUnitTests'
            }
        }
        stage('BUILD') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}