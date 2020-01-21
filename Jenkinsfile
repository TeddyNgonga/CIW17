pipeline {
  agent any 
  stages {
    stage('Maven: clean project') {
              steps {
               bat "C:\\Program Files\\apache-maven-3.6.3-bin\\apache-maven-3.6.3\\bin\\mvn clean"
              }
    }
	stage('Maven: build project') {
              steps {
               bat "C:\\Program Files\\apache-maven-3.6.3-bin\\apache-maven-3.6.3\\bin\\mvn install"
              }
    }
	stage('Maven: test project') {
              steps {
               bat "C:\\Program Files\\apache-maven-3.6.3-bin\\apache-maven-3.6.3\\bin\\mvn test"
            }
    }
    
  }
}


