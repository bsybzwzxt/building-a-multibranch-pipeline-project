pipeline {
    agent {
        docker {
            image 'node'
            args '-p 3000:3000 -p 5000:5000'
        }
    }
    stages {
        stage('Build') {
          steps {
              sh 'node -v'
              sh 'npm -v'
              sh 'npm install'
              sh 'npm build'
          }
        }
    }
}
