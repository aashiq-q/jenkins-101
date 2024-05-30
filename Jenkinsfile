pipeline {
    agent any
    triggers {
        cron('* * * * *') // Run every minute
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
                sudo apt-get update
                sudo apt-get install python3 python3-pip
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
