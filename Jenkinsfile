pipeline {
  agent any
  stages {

    

    stage('build') {
      steps {
        script {
          echo 'build started'
		  sh 'mvn clean install '
        }
      }
    }
	
	stage('atifacts') {
      steps {
        script {
          echo 'push the package into artifact'
		  
		  sh 'mvn clean deploy'
        }
      }
    }
	

  }
}
