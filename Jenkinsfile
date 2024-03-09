pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // python prer.py //error
                    sh 'g++ PES1UG21CS106-1.cpp -o PES1UG21CS106-1'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './PES1UG21CS106-1'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
    post {
          failure {
              echo 'Pipeline failed'
          }
      }
}
