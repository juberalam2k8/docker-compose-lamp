pipeline {
   agent any

   stages {
      stage('Deploy') {
         steps {
            git 'https://github.com/sprintcube/docker-compose-lamp.git'
            pushd docker-compose-lamp/
            git fetch --all
            git checkout 7.3.x
            xcopy sample.env .env
            bat 'docker-compose build'
            bat 'docker-compose up'
         }
      }
   }
}
