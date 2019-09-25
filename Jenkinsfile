pipeline {
    agent {
        docker { image 'ubuntu' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
        stage ('Test2') {
            steps {
                sh 'echo "Hello from docker container"'
            }
        }
    }
}
