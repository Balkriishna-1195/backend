pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
       timeout(time: 30, unit: 'MINUTES')
       disableConcurrentBuilds()
       ansiColor('xterm')
    }
    stages {
        stage('init') {
            steps {
                sh """
                  echo "this is testing"
                """
            }
        }
    }
     post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success { 
            echo 'I will run when pipeline success'
        }
        failure { 
            echo 'I will run when pipeline failure'
        }
    }
}