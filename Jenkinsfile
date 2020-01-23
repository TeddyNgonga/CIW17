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
    
  }
}

