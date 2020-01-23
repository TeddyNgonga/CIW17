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
    stage('push back'){

         steps {

      checkout(

[$class: 'GitSCM', branches: [
					[name: '*/master']],
					doGenerateSubmoduleConfigurations: false, 
					extensions: [], 
					submoduleCfg: [], 
					userRemoteConfigs: [
					[credentialsId: '83ce4725-8966-455e-b7d5-47c6a4a5222b', 
					url: 'https://github.com/20chix/CIW17']]])
    
    
emailext body: 'dwdwdw', subject: 'dwdwd', to: 'hadi.elme92@gmail.com' 


    }
    }
  }
}

