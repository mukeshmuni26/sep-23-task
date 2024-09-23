pipeline {
  agent any 
     stages {
          stages('validation') {
               steps { 
                        echo "checking for 'pom.xml' file for maven project"
                        bat ' mvn validation'
       }
   }
    stage('build') {
          steps { 
                   echo " making build for maven project "
                   bat ' mvn clean package'
       }
   }
     stage('execute') {
           steps {
                   echo " executing the build to get the output for maven project"
                   bat 'java -jar target/MavenProject-0.0.1-SNAPSHOT.jar'
       }
    }
  }
}
