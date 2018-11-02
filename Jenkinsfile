env.mvnHome = '/usr/share/maven3'
node('any') {
   
   
   stage('Preparation') { // for display purposes
      
      git 'https://github.com/jglick/simple-maven-project-with-tests.git'
        
      
   }
   stage('Build') {
      
      if (isUnix()) {
         sh "'${mvnHome}/bin/mn' clean install"
      } else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
   stage('publish') {
     echo 'vdjhvbhjdsb'
   }
   

}
