pipeline {
    agent any
    triggers {
        pollSCM('* * * * *') // Poll SCM every minute (optional if you have webhooks)
        cron('H 17 * * *\nH/10 * * * *') // Cron triggers: once at 5 PM + every 10 min spread
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo "Building branch: ${env.BRANCH_NAME}"
                echo 'Building after GitHub push or polling...'
            }
        }
        stage('Run') {
            steps {
                echo "Pipeline triggered at ${new Date()}"
            }
        }
    }
}


