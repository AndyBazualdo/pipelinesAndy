/*
//pipeline + my container
pipeline {
        agent {
            docker { image 'gato756/awt04webservice_1.0:1.0' }
        }
        stages {
            stage('Test') {
                steps {
                    sh 'uname -a'
                }
            }
            stage ('Test2') {
                steps {
                    sh 'echo "Hello from docker container"'
                }
            }
        }
}
*/


pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker { image 'gato756/awt04webservice_1.0:1.0' }
            }
            steps {
                echo 'Building..'
                sh 'cd /AWT04-WebService/ && ls -al && pwd'
                sh './gradlew build'
            }
        }
    }
}

/*
pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker { image 'gato756/awt04webservice_1.0:1.0' }
                //dockerfile true
            }
            steps {
                echo 'Building..'
                @docker.image('gato756/awt04webservice_1.0:1.0')inside(" ./gradle build")
            }
        }
    }
}
*/