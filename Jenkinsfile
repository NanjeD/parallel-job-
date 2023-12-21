pipeline{
	agent any 
	stages{
		stage{
			parallel{
				stage('1-action1'){
					steps{
						sh 'action one'
					}
				}
				stage('1-action2'){
					steps{
						sh 'action two'
					}
				}
			}
		}
		stage('2-action1'){
			steps{
				sh 'action3'
			}
		}
		stage{
			parallel{
				stage('3-action1'){
					steps{
						sh 'action1 of 4'
					}
				}
				stage('3-action2'){
					steps{
						sh '3-action2 of 4'
					}
				}
				stage('3-action3'){
					steps{
						sh '3-action3 of 4'
					}
				}
			}
		}
	}
