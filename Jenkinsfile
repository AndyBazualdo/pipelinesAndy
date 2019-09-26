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


pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker { image 'gato756/awt04webservice_1.0:1.0' }
                //agent { dockerfile true }

            }
            steps {
                docker.image('gato756/awt04webservice_1.0:1.0').inside {
                    sh 'pwd'
                }
                echo 'Building..'
                sh 'pwd'
                sh 'echo $JAVA_HOME'
                sh 'ls -al'
                //sh './gradle build'
                echo 'finish building'
            }
        }
    }
}



