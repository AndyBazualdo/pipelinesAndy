/*pipeline {
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
            steps {
                echo 'Building..'
            }
        }
    }
}



