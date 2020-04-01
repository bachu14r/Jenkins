pipeline {
   agent any
   stages {
     stage ('Pull the code from github') {
       steps {
          git branch: 'master', url: "https://github.com/bachu14r/maven-project-1.git"
       }
     }
   }
      stage ('maven install') {
        steps {
            tool: Maven,
            pom : maven-project-1/pom.xml
            goals: 'clean install'
         }
      }
}
