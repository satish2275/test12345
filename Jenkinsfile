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
         
//         when {
           expression {
              currentBuild.result == NULL || currentBuild.result == "SUCCESS"
    
                    }                
             } //

          echo "Build URL is ${env.BUILD_URL}"
   }
}

  }
}
