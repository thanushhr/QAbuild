pipeline {
  agent any
stage ('TEST PARALLEL') {
    parallel {
    stage ('BUILD1') {
      steps {
        echo "This is BUILD1" 
        sh '''
          echo "p1"
          exit 0
          '''
        }
      } 
	  stage ('BUILD2') {
      steps {
        echo "This is BUILD2" 
        sh '''
          echo "p1"
          exit 0
          '''
        }
      } 
	  stage ('BUILD3') {
      steps {
        echo "This is BUILD3" 
        sh '''
          echo "p1"
          exit 0
          '''
        }
      } 
	  stage ('BUILD4') {
      steps {
        echo "This is BUILD4" 
        sh '''
          echo "p1"
          exit 0
          '''
        }
      } 
      stage ('BUILD5') {
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
