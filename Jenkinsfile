pipeline {
    agent any

    stages {
        stage('Preparation') {
            step {
            echo "My first stage"

            }
        }

        stage('Build') {
            when {
                expression {
                    branch = 'xr-dev1'
                }
            }
            step {
            echo " I am Building the python files"

            }
        }

        stage('Testing') {
            step {
            echo " I am testing the python files"

            }
        }
    }
}