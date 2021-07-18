pipeline {
   agent any  'M2_HOME'
   tools {
     maven
   }
   stages {
      stage('Build step'){
         steps {
          sh 'mvn clean'
          sh 'mvn install'
          sh 'mvn package'
         }
      }
      stage('test'){
         steps {
          echo "test step"
          sh 'mvn test'  
         }
      }
      stage('deploy'){
         steps {
          echo "deploy step"
          sleep 10  
         }
      }
      stage('docker'){
         steps {
          echo "image step"
          sleep 10  
         }
      }
   }

}
