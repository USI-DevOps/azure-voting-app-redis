pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Docker Build') {
		 steps {
			pwsh(script: 'docker images -a')
			pwsh(script: """
				cd azure-vote/
				docker images -agentdocker build -t jenkins-pipeline .
				docker images -a
				cd ..
				""")
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
   }
}
