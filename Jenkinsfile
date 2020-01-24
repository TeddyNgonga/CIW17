pipeline {
  agent any 
      tools { 
        maven 'maven' 
    }
	
  stages {
					
				
    stage('Maven: clean project') {
              steps {
				bat """cd "C:\\Users\\212610402\\eclipse-workspace\\CI_W17" 

				mvn clean
                
                """
              }
    }
	stage('Maven: package project') {
              steps {
				bat """

				mvn package
                
                """
              }
    }
	stage('Maven: test project') {
              steps {
				bat """

				mvn test
                
                """
              }
    }
    stage('Send email notification'){
        steps{

            mail bcc: '', 
            body: "<b>Edison CI project </b><br>Project: ${env.JOB_NAME} <br>Build Number: ${env.BUILD_NUMBER} <br> URL for build: ${env.BUILD_URL}", 
            cc: '', 
            charset: 'UTF-8', 
            from: 'hadi.elme92@gmail.com', 
            mimeType: 'text/html', 
            replyTo: '', 
            subject: "EDISON CI W17 : JOB Name -> ${env.JOB_NAME}", 
            to: "hadi.elme92@gmail.com";  

        }
    }


  

      stage('push_git'){

          steps{

      withCredentials([
              [$class: 'UsernamePasswordMultiBinding', 
              credentialsId: 'githubtest', 
              usernameVariable: '20chix',
              passwordVariable: 'dip2chill']]) {
      bat"git push https://github.com/20chix/CIW17"
        }
          }

      }
      post {
        always {
           // archiveArtifacts artifacts: 'build/libs/**/*.jar', fingerprint: true
            junit 'target//surefire-reports/*.xml'

            recordIssues enabledForFailure: true, tools: [mavenConsole(), java(), javaDoc()]



        }
    }


}

