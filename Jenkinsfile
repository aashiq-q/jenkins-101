pipeline {
    agent{
        docker { image 'python:3.9-alpine3.20' }
    }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                echo "doing building stuff.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                python3 helloworld.py
                apt-get update
                apt-get install python3 python3-pip
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
