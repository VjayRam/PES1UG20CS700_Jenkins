pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o myprogramm myprogramm.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './myprogramm'
            }
        }
        stage('Deploy') {
          steps {
              sh 'echo "Deployment completed successfully"'
          }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed!!'
        }
    }
}
