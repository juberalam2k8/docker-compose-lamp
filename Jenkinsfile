pipeline {
   agent any

   stages {
      stage('Deploy') {
         steps {
            git 'https://github.com/sprintcube/docker-compose-lamp.git'
            xcopy sample.env .env
            bat 'docker-compose build'
            bat 'docker-compose up'
         }
      }
   }
}
