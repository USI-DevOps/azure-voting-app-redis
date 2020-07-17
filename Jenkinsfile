pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Build') {
	 steps {
	     echo 'Hello World'
	  }
      }
      stage('Test') {
	 steps {
	     echo 'Hello World'
	 }
      }
      stage('Docker Build') {
	 steps {
	     echo "Docker build started"
	 }
      }
    }
}
