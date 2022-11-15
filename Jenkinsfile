pipeline {
    agent any
    stages {
        stage ('build')  {
            agent{
                docker { image 'bennun1docker/eido-task-15-11-22:latest' }
            }
            steps {
                sh 'python3 main.py'
            }
    
        }
        stage('check') {
            agent{
                docker { image 'node:16.13.1-alpine' }
            }
            steps {
                sh 'python main.py'
            }
        }
        
    }
}

