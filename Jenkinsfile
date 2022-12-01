pipeline {
  agent any
	stages {
stage ('TEST PARALLEL') {
    parallel {
    stage ('BUILD C') {
      steps {
        echo "This is BUILD1" 
        sh '''
          make
          exit 0
          '''
        }
      } 
	  stage ('MAVEN') {
		  agent { label 'node1' }
      steps {
        echo "This is BUILD2" 
        sh '''
          echo "p1"
          exit 0
          '''
        }
      } 
	  stage ('APACHE ANT') {
      steps {
        echo "This is BUILD3" 
        sh '''
          echo "p1"
          exit 0
          '''
        }
      } 
	  stage ('SBT') {
      steps {
        echo "This is BUILD4" 
        sh '''
          echo "p1"
          exit 0
          '''
        }
      } 
      stage ('MSBuild') {
      steps {
        echo "This is BUILD5" 
        sh '''
          echo "p2"
          exit 0
          '''
          }
        }
      }
    }  
	}
}
