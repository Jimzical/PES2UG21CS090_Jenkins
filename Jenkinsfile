pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
              build 'PES2UG21CS090-1'
              sh 'g++ main2.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            
            }
        }
        stage('Deploy') {
            steps {
              echo 'Deployed!'
            }
        }
    }

    post {
        failure {
            error 'Pipeline Failed'
        }
    }
}
