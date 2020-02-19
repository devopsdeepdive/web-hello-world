#!groovy
node ("master") {
    checkout scm
    stage "clean test" {
	sh 'chmod +x ./gradlew'
    sh './gradlew clean test'
    }
    stage "archive" {      
	sh './gradlew package'	
	}
}
