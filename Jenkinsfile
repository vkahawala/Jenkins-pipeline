pipeline {
    environment {
        BUILD_SCRIPTS_GIT="https://github.com/vkahawala/Jenkins-pipeline.git"
        BUILD_SCRIPTS='mypipeline'
        BUILD_HOME='/var/lib/jenkins/workspace'
    }
    agent any
    stages {
        stage('Build') {
            steps {
                sh "chmod +x $WORKSPACE/build.sh"
                sh "$WORKSPACE/build.sh"
            }
        }
    }
}