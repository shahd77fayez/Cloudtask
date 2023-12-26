pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the Git repository
                git 'https://github.com/shahd77fayez/Cloudtask.git'
            }
        }

        stage('Execute Bash Script') {
            steps {
                script {
                    def output = bat(script: 'CommandCloudTask.sh', returnStdout: true, encoding: 'UTF-8').trim()
                    echo "Script Output: ${output}"
                }
            }
        }
    }
}
