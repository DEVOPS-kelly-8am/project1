pipeline {
  agent any
  stages {

    stage('checkout') {
      steps {
        script {
          bat 'git clone https://github.com/DEVOPS-kelly-8am/project1.git '
        }
      }
    }

    stage('build') {
      steps {
        script {
          echo 'build started'
		  bat  'mvn clean install '
        }
      }
    }
	
	stage('atifacts') {
      steps {
        script {
          echo 'push the package into artifact'
		  
		  bat 'mvn clean deploy'
        }
      }
    }
	

  }
}
