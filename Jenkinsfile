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
