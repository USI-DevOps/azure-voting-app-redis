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
	     pwsh(script: "docker images -a")	     
	     pwsh(script: """
		cd azure-vote/
		docker images -agentdocker build -t jenkins-pipeline .
		docker images -a
		cd ..
		""")
	 }
      }
    }
}
