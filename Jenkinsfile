pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building...' // Simple shell command or step
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
         stage('deploy') {
            steps {
                echo 'deploying...'
            }
        }
    }
    
}