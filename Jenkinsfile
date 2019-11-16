node{
     def app
     stage('Checkout'){
       git 'https://github.com/sprintcube/docker-compose-lamp.git'
       }
     stage('Compile and Package'){
       def JAVA_HOME = tool name: 'jdk-11.0.4', type: 'jdk'
       cd docker-compose-lamp/
       git fetch --all
       git checkout 7.3.x
       cp sample.env .env
       app = docker-composer.build("juberalam2k8/docker-compose-lamp")
       
       
     }

}
