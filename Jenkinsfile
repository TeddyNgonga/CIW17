pipeline {
  agent any 
  stages {
    stage('Maven: clean project') {
              steps {
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
