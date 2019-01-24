pipeline {
    agent {
        docker {
            image 'node'
            args '-p 3000:3000 -p 5000:5000'
        }
    }
    stages {
        stage('nginx') {
            agent {
                docker {
                    image 'nginx'
                    args '-p 8000:8000 -p 9000:9000'
                }
            }
        }
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
