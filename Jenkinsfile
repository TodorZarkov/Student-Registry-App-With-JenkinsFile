pipeline{
    agent any
    stages{
        stage("NPM Install"){
            steps{
                bat 'npm install'
            }
            
        }
        stage("NPM Audit"){
            steps{
                bat 'npm audit'
            }
        }
        stage("Run integration tests"){
            steps{
                bat 'npm test'
            }
        }
        stage("Deploy"){
            steps{
                input message: 'Approve deployment?', ok:  'Deploy to production'
                echo 'DEPLOY'
            }
        }
    }
}
    