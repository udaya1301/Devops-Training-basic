pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
            echo 'Hello World hi'
         }
      }
      stage('Maven Build') {
        steps {
          withMaven(maven: 'mvn') {
              sh 'mvn clean package'
          }
           archiveArtifacts 'target/devops.war'
        }    
     }
   }
}
