pipeline {
    agent any
    triggers {
        pollSCM('* * * * *') // Optional: poll SCM every minute; remove if using webhooks only
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm // Use Jenkins' configured SCM for this branch in Multibranch Pipeline
            }
        }
        stage('Build') {
            steps {
                echo "Building branch: ${env.BRANCH_NAME}"
                echo 'Building after GitHub push or polling...'
            }
        }
    }
}


