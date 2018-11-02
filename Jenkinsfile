env.mvnHome = '/usr/share/maven3'
node {
   
   
   stage('Preparation') { // for display purposes
      
      checkout scm
      
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
