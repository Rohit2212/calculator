pipeline{
    agent any;
    
    environment{
        //environment variables
    }
    
    tools{
        nodejs 'jenkins-jobs-node'
    }
    
    stages{
        stage('Initialize'){
            steps{
                sh '''
                    npm install
                '''
            }
        }
        stage('Unit Tests'){
            steps{
                sh '''
                    npm run test -- --watchAll=false
                '''
            }
        }
        stage('Build'){
            steps{
                sh '''
                    npm run build
                '''
            }
        }
    }
}