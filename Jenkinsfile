pipeline {
  agent any 
     stages {
          stage('validation') {
               steps { 
                        echo "checking for 'pom.xml' file for maven project"
                        sh ' mvn validation'
       }
   }
    stage('build') {
          steps { 
                   echo " making build for maven project "
                   sh ' mvn clean package'
       }
   }
     stage('execute') {
           steps {
                   echo " executing the build to get the output for maven project"
                   sh 'java -jar target/MavenProject-0.0.1-SNAPSHOT.jar'
       }
    }
  }
}
