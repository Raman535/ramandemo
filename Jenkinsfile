pipeline {
agent {
  label 'cherry'
}    
     environment {
        // Using returnStdout
        CC = """${sh(
                returnStdout: true,
                script: 'echo "clang"'
            )}""" 
        // Using returnStatus
        EXIT_STATUS = """${sh(
                returnStatus: true,
                script: 'exit 1'
            )}"""
    }

    stages {
        stage('checkout') {
           
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'xr-dev']], extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir: '/home/cherry/ramandemo']], userRemoteConfigs: [[credentialsId: '90e8f891-27fc-47c0-9ec6-db25830d3724', url: 'https://github.com/Raman535/ramandemo']]])
                 echo " I am Building the python files"

            }
        }

        stage('Testing') {
            steps {
                echo " I am testing the python files ${CC}"

            }
        }
    }
}
