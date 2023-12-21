pipeline{
    agent any 
    stages {
        stage ('stepone'){
            parallel{
                stage ('stepone stage one'){
                    steps{
                        echo "This is stepone stage one"
                    }
                }
                stage ('stepone stage two'){
                    steps{
                        echo " This is stepone stage two"
                    }
                }
                stage ('stepone stage three'){
                    steps{
                        echo "This is step three"
                    }
                }
            }
        }
        stage('steptwo'){
            parallel{
                stage('steptow stage one'){
                    steps{
                        echo "This is steptwo stage one"
                    }
                }
                stage('steptwo stage two'){
                    steps{
                        echo "This is steptwo stage two"
                    }
                }
            }
        }
        stage('stepthree'){
            steps{
                echo "This is step three"
            }
        }
        stage('stepfour'){
            parallel{
                when
                branch 'feature'
                stage('stepfour stage'){
                    steps{
                        echo "The step will fail"
                    }
                }
                stage('stepfour'){
                    when 
                    branch 'main'
                    steps{
                        echo "this is stepfour stage two"
                    }
                }
            }
        }
        stage('stepsix'){
            steps{
                echo " This is after the restriction"
            }
        }
    }
}
