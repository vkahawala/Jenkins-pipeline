pipeline {
environment {
BUILD_SCRIPTS_GIT="https://github.com/vkahawala/Jenkins-pipeline.git"
BUILD_SCRIPTS='mypipeline'
BUILD_HOME='/var/lib/jenkins/workspace'
}
agent any
stages {
stage('Checkout: Code') {
steps {
sh "mkdir -p $WORKSPACE/repo;\
git config --global user.email 'venura.kahawalage@mclaren.com';\
git config --global user.name 'vkahawala';\
git config --global push.default simple;\
git clone $BUILD_SCRIPTS_GIT repo/$BUILD_SCRIPTS"
sh "chmod -R +x $WORKSPACE/repo/$BUILD_SCRIPTS"
}
}
stage('Build') {
steps {
sh "chmod +x $WORKSPACE/repo/$BUILD_SCRIPTS/build.sh"
sh "$WORKSPACE/repo/$BUILD_SCRIPTS/build.sh"
}
}
}
}