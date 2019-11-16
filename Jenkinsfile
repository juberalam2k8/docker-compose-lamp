node{
     def app
     stage('Checkout'){
       git 'https://github.com/sprintcube/docker-compose-lamp.git'
       }
     stage('Compile and Package'){
       def JAVA_HOME = tool name: 'jdk-11.0.4', type: 'jdk'
       app = docker.build("juberalam2k8/docker-compose-lamp")
     }

}
