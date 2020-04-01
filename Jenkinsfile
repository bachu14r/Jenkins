pipeline {
   agent any
   tools {
       maven 'Maven 3.5.2'
       jdk 'jdk 1.8.0'
   }
   stages {
     stage ('Pull the code from github') {
       steps {
          git branch: 'master', url: "https://github.com/bachu14r/maven-project-1.git"
       }
     }
   }
      stage ('Intialize') {
        steps {
            sh '''
              echo "PATH = ${PATH}"
              echo "M2_HOME" = $(M2_HOME)
        }
      }
      stage ('Build') {
        steps {
            sh 'mvn clean install'
         }
      }
}
