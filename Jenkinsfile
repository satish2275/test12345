pipeline {
   agent any
   tools {
           maven 'apache-maven-3.0.1'
         }
   stages {
    stage ('Download') {
      steps {
          git 'https://github.com/satish2275/mavenproject.git'
            }
        }

    stage ('Build') {
      steps {
          sh 'mvn package'
          echo "Build location is : ${env.BUILD_URL}"
             }      

         }     
}
}
