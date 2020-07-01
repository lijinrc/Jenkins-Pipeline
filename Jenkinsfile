pipeline {
	agent {
		label 'master'
	}
	stages{
		stage ('Dev') {
			steps {
				echo "On Development"
			}
		}
		stage ('Test') {
			steps {
				echo "On Test"
			}
		}
		stage ('Parallel-Stage-Prod') {
			parallel {
				stage ('Stage') {
					agent {
						label 'windows10'
					}
					steps {
						echo "On Stage"
					}
				}	
				stage ('Prod') {
					agent {
						label 'linux-mint'
					}
					steps {
						echo "On Prod"
					}
				}
			}
		}


	}
}
