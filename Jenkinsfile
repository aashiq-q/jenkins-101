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
                cd myapp
                python3 hello.py
                python3 hello.py --name=Brad
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
