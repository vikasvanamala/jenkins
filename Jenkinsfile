pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        course = "jenkins"
    }
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                        echo 'Building...'
                        echo $course 
                    """    
                }    
            }
        }
        stage('Test') {
            steps {
                 script {
                    sh """
                        echo 'testing...' 
                    """    
                }  
            }
        }
         stage('deploy') {
            steps {
                 script {
                    sh """
                        echo 'deploying...' 
                    """    
                }  
            }
        }
    }
    post {
        always {
            echo 'i will always say hello'
            cleanWs()
        }
    }
}