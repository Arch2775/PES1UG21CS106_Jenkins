pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Arch2775/PES1UG21CS106_Jenkins.git'
            }
        }

        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    sh 'g++ -o my_executable ${WORKSPACE}/main/hello2.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Print output of the compiled .cpp file
                    sh './my_execute'
                }
            }
        }

        stage('Deploy'){
            steps {
                script {
                    echo 'Deploy successful'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
