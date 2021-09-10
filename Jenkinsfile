pipeline {
    agent any

    stages {
        stage('Preparation') {
            steps {
            echo "My first stage"

            }
        }

        stage('Build') {
            when {
                expression {
                    branch = 'xr-dev'||'test'
                }
            }
            steps {
                withCredentials([usernamePassword(credentialsId: '90e8f891-27fc-47c0-9ec6-db25830d3724', passwordVariable: 'pass', usernameVariable: 'user')]) {
                    git branch: 'xr-dev', credentialsId: '90e8f891-27fc-47c0-9ec6-db25830d3724', url: 'https://github.com/Raman535/ramandemo'}
                    echo " I am Building the python files"

            }
        }

        stage('Testing') {
            steps {
            echo " I am testing the python files"

            }
        }
    }
}
