pipeline {
    agent any
    stages {
       stage('build') {
          steps {
             echo 'Notify GitLab'
             echo 'build step goes here'
          }
       }
       stage(test) {
         when {
          branch 'xr-dev'
         }
           steps {
               echo 'Notify GitLab'
               echo 'test step goes here'
             

           }
       }
    }
 }

