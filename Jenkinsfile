pipeline {
    agent none
    stages {
        stage('Build') {
          steps {
              sh 'node -v'
              sh 'npm -v'
              sh 'npm install'
              sh 'npm run build'
          }
        }
    }
}
