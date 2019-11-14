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
                sh 'chmod -R 777 ./myCheck.sh '
                sh './myCheck.sh'
                echo 'Build is Complete'
            }
        }
   }
}
      
