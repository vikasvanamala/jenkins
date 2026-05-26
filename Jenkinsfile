pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        course = "jenkins"
    }
    options {
        timeout(time: 10, unit: 'MINUTES') 
        disableConcurrentBuilds()
    }
    // parameters {
    //     string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    //     text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    //     booleanParam(name: 'DEPLOY', defaultValue: false, description: 'Toggle this value')
    //     choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    //     password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    // }
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                        echo 'Building...'
                        echo $course 
                        
                        echo "Hello ${params.PERSON}"
                        echo "Biography: ${params.BIOGRAPHY}"
                        echo "Toggle: ${params.DEPLOY}"
                        echo "Choice: ${params.CHOICE}"
                        echo "Password: ${params.PASSWORD}"
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
            // input {
            //      message "Should we continue?"
            //      ok "Yes, we should."
            //      submitter "alice,bob"
            //      parameters {
            //         string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
            //     }
            // }
            // when { 
            //     expression { "$params.DEPLOY" == "true" }
            // }
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