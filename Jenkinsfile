pipeline {
    agent any

    stages {
        stage('testing') {
            steps {
                echo 'Hello World from test stage'
            }
        }
        stage ('git clone'){
            steps {
                sh ('git --version')
            }
        }
        stage('docker build') {
            steps {
                echo "stage for building images started"
                sh( 'pwd' )
                sh( 'docker version' )
                sh( 'ls' ) 
                sh('docker build -t sample:v1 . --no-cahe')
            }
        }
        stage('docker run') {
            steps {
                echo "stage for running containers started"
                sh( 'docker run --name docker-con -d -p 80:80 sample:v1 ' )
            }
        }
    }
}
