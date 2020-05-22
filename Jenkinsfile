pipeline {
  agent any
  stages {
        stage('checkout') {
            steps { 
                checkout scm
            }  
        }
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'chmod -R 777 jq-osx-amd64.dms'
                sh 'chmod -R 777 ./myCheck.sh'
                sh './myCheck.sh Input.json'
                echo 'Build is Complete'
            }
        }
        stage('Testing') {
           steps {
                echo 'Testing..'
                sh 'cat Input.json'
            }
        }
   }    
}
      
