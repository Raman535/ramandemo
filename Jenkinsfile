pipeline {
    agent any

    stages {
        stage('Preparation') {
            echo "My first stage"
        }

        stage('Build') {
            when {
                expression {
                    branch = 'xr-dev1'
                }
            }
            echo " I am Building the python files"
        }

        stage('Testing') {
            echo " I am testing the python files"
        }
    }
}