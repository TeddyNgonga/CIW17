pipeline {
  agent any 
  stages {
    stage('Maven: clean project') {
              steps {
			   bat "set path=C:\\Program Files\\apache-maven-3.6.3-bin\\apache-maven-3.6.3\\bin:%path%;"
               bat "mvn clean"
              }
    }
	stage('Maven: build project') {
              steps {
               bat "mvn install"
              }
    }
	stage('Maven: test project') {
              steps {
               bat "mvn test"
            }
    }
    
  }
}


