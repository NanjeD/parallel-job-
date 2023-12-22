pipeline{
    agent any 
    stages{
      stage('1-git clone'){
        steps{
       sh 'whoami'
        }
      }
      stage('2-system check'){
        steps{
          sh ' echo "walk...." '
          sh 'lscpu'
        }
      }
      stage('3-memory check'){
        steps{
          sh ' echo "walk...." '
          sh 'cat /etc/passwd | grep ubuntu'
        }
      }
      stage('4-os stats'){
        steps{
          sh ' echo "walk...." '
          sh 'whoami'
        }
      }
      stage('5-last movement'){
        steps{
          sh ' echo "The final level"'
          sh 'pwd'
        }
      }
      stage('6-webhook testing'){
        steps{
          sh ' echo "walk...." '
          sh 'ps -ef'
        }
      }
    }
  }
