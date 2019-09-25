pipeline {
    agent {
        //docker { image '' }
        dockerfile true
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
