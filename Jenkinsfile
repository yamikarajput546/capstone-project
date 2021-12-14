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
           

         when {
        branch 'dev'
            }
         steps
            {
                sh 'mvn clean '

            }
       }
       stage("test"){
           

          when{
             branch 'test'
          }
       

         steps
            {
                sh 'mvn clean test'
            }

   }

   stage("packaging"){
      when{
             branch 'prod'
          }
           

         steps
            {
                sh 'mvn package'
            }
       }

   }
}
