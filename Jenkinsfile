pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Build stage for ${env.BRANCH_NAME}"
            }
        }

        stage('Test') {
            steps {
                sh './test.sh'
            }
        }

        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                echo "Deploying from MAIN branch only"
            }
        }
    }
}

