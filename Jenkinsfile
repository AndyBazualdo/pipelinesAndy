/*
//pipeline + my container
pipeline {
        agent {
            docker { image 'gato756/awt04webservice_1.0:1.0' }
            //dockerfile true
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

/*
pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker { image 'gato756/awt04webservice_1.0:1.0' }
            }
            steps {
                echo 'Building..'
                sh 'ls -al'
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
                //dockerfile true
            }
            steps {
                echo 'Building..'
                docker.image('gato756/awt04webservice_1.0:1.0')inside("sh './gradle build'")
            }
        }
    }
}

