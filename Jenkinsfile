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
                stage('stepfour stage one'){
                    when{
                        branch 'feature'
                    }
                    steps{
                        echo "I am sleeping"
                    }
                }
                stage('stepfour'){
                    when{
                        branch 'main'
                    }
                    steps{
                        echo "This is up"
                    }
                }
            }
        }
    }
}
