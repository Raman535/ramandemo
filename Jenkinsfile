pipeline {
    agent any
    options {
  timestamps
}
    stages {
       stage('build') {
          steps {
             echo 'Notify GitLab'
             echo 'build step goes here'
          }
       }
       stage(test) {
         when {
          branch 'xr-dev1'
         }
           steps {
               echo 'Notify GitLab'
               echo 'test step goes here'
             

           }
       }
    }
 }

