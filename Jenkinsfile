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
    stages {
        stage ('1-clone'){
            steps{
                sh ' cat /etc/passwd'
            }
        }
        stage('2-parallel'){
            parallel{
                stage('1-subjob1'){
                    steps {
                        sh 'lscpu'
                    }
                }
                stage ('2-subjob2'){
                    steps {
                        sh 'ps -ef'
                    }
                }
            }
        }
        stage('3-codetest'){
            steps {
                sh 'pwd && whoami'
            }
        }
        stage ('4-closing'){
            when {
                branch 'feature'
            }
            steps{
                sh 'free -g'
                echo "We are done"
            }
        }
        stage ('5-codeanalysis'){
            parallel{
                stage('5-subjob1'){
                    steps{
                        sh 'df -h'
                        echo "Yes we are going ahead"
                    }
                }
                stage('5-subjob2'){
                    steps{
                        sh 'htop'
                        echo " This is the end of the code"
                    }
                }
            }
        }
    }
}