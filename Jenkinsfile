pipeline {
    agent any

    stages {
        stage('testing') {
            steps {
                echo 'Hello World from test stage'
            }
        }
        stage ('git clone')
        stage('docker build') {
            steps {
                echo "dokcer testing started"
                sh( 'pwd' )
                sh( 'docker version' )
                sh( 'ls' ) 
            }
        }
    }
}
