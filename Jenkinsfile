pipeline {
   agent any

   stages {
	
	  stage('clone repo) {
         steps {
            git(
				url: 'https://github.com/kumaraswamym/web-hello-world',
				branch: "master"
    )
         }
      }
      stage('clean test') {
         steps {
            sh 'chmod +x ./gradlew'
			sh './gradlew clean test'
         }
      }
	  stage('archive') {
         steps {
            sh './gradlew package'
         }
      }
   }
}
