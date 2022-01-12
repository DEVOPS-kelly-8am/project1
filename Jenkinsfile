pipeline {
  agent any
  stages {

    stage('checkout') {
      steps {
        script {
          sh 'git clone https://github.com/DEVOPS-kelly-8am/project1.git '
        }
      }
    }

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
