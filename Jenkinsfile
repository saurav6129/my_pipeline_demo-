pipeline {
	
	agent any
	
	stages {
		
		stage("One") {
			
			
			steps {
				echo 'Hi this is Saurav...'
			
			}
		}
		stage("Two") {

			
			steps {
				input('Do you want to proceed further ?')
			}
		}
		
	
		stage("Three") {
		
			when {
				not {
					branch 'master'
				
				}
			}
			
			steps {
				echo 'Hello ...'
			}
		}
		
		
		stage("Four") {
		
			parallel {
				stage('Unit Test'){
					steps {
						echo "Running the unit test ..."
					}
				}
			
			
				stage('Integration Test') {
					
					steps {
						echo 'Running the integration test...'
					
					}
					
				}
			}
		
		}
		
		

	}

}