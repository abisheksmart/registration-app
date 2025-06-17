pipeline {
    agent any
    triggers {
        pollSCM('* * * * *') // Optional: poll every minute (you can remove or adjust)
    }
    stages {
        stage('Build') {
            steps {
                echo "Building branch: ${env.BRANCH_NAME}"
                echo 'Building after GitHub push...'
            }
        }
    }
}
