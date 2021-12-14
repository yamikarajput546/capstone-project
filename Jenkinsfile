pipeline {
   agent any
   tools {
       maven 'maven'
       jdk 'Java'
   }
  // environment {
    //  dockerhub=credentials('dockerhub')
 //  }
   stages{
       stage("clean"){
         
              steps
              {
                 sh 'mvn clean'
              }
          
       }
       stage("test"){
           
         when {
        branch 'myBranch'
            }
         steps
            {
                sh 'mvn test'
            }

   }
   stage("packaging"){
           
         steps
            {
                sh 'mvn package'
            }
       }
   }
}
