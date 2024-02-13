pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from version control (e.g., Git)
                checkout scm
            }
        }

        stage('Execute Script') {
            steps {
                // Run your script file
                script {
                    
			chmod +x test.sh
			sh './test.sh'
                }
            }
        }
    }

    post {
        success {
            echo 'Script executed successfully'
        }

        failure {
            echo 'Script execution failed'
        }
    }
}

