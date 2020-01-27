pipeline {
  agent any 

  stages {
					
				
    stage('Maven: clean project') {
              steps {
						bat """ 

				mvn install
                
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
