pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o myprogram myprogram.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './myprogram'
            }
        }
        stage('Deploy') {
          steps {
              sh 'echo "Deployment completed successfully"'
          }
        }
    }
    
    post {
        always {
            script {
                def result = currentBuild.result
                if (result == 'FAILURE') {
                    echo 'Pipeline failed'
                }
            }
        }
    }
}
