pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS268 PES1UG20CS268.cpp'
                build job: 'PES1UG20CS268-1'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES1UG20CS268'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
