pipeline {
    agent {
        docker { image 'gato756/awt04webservice_1.0' }
        //dockerfile true
    }
    stages {
        stage('Test') {
            steps {
                sh 'echo Hello'
            }
        }
        stage ('Test2') {
            steps {
                sh 'echo "Hello from docker container"'
            }
        }
    }
}
