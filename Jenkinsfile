pipeline {
   agent any

   stages {
      stage('Deploy') {
         steps {
            git 'https://github.com/sprintcube/docker-compose-lamp.git'
            bat 'docker-compose build'
            bat 'docker-compose up'
         }
      }
   }
}
