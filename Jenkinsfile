pipeline {
  agent any
	stages {
stage ('TEST PARALLEL') {
    parallel {
    stage ('BUILD C') {
      steps {
        echo "This is C Build" 
        sh '''
          make
          exit 0
          '''
        }
      } 
	  stage ('MAVEN') {
		  agent { label 'node1' }
      steps {
        echo "This is Maven Build" 
        sh '''
          mvn package
          exit 0
          '''
        }
      } 
	  stage ('GRADLE') {
      steps {
        echo "This is Gradle Build" 
        sh '''
          echo "hello gradle"
          exit 0
          '''
        }
      } 
	  stage ('APACHE ANT') {
      steps {
        echo "This is Ant Build" 
        sh '''
          echo "p1"
          exit 0
          '''
        }
      } 
      stage ('MSBuild') {
      steps {
        echo "This is MS Build" 
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
