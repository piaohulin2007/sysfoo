pipeline{

  agent any

  tools{
    maven 'Maven 3.6.3'
  }

  stages{

    stage('build'){
      step{
        sh 'mvn compile'
      }
    }
  
    stage('Maven project test'){
      step{
        sh 'mvn clean test'
      }
    }
  
    stage('Maven project package'){
      step{
      	sh 'package -DskipTests'
      }
    }
  }
} 
