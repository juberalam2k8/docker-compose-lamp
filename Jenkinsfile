node{
     def app
     stage('Checkout'){
       git 'https://github.com/sprintcube/docker-compose-lamp.git'
       }
     stage('Compile and Package'){
       def JAVA_HOME = tool name: 'jdk-11.0.4', type: 'jdk'
       def mvnHome = tool name: 'apache-maven-3.6.2', type: 'maven'
       bat "${mvnHome}/bin/mvn clean package"
       app = docker.build("juberalam2k8/camunda-spring-boot-amqp-microservice-cloud-example")
     }

}
