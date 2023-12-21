pipeline{
    agent any 
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
                        echo " This is the end of the build"
                    }
                }
            }
        }
    }
}
