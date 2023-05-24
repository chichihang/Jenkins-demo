pipeline {
    agent {
        node {
           label 'docker-agent-python' 
        }
    }
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('build') {
            steps {
                echo 'Building'
            }
        }
        stage('print') {
            steps {
                sh '''
                python3 hello.py
                '''
            }
        }
    }
}
