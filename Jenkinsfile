pipeline{

  agent any

  tools{
    maven 'Maven 3.6.3'
  }

  stages{

    stage('build'){
      steps{
        sh 'mvn compile'
      }
    }
  
    stage('Maven project test'){
      steps{
        sh 'mvn clean test'
      }
    }
  
    stage('Maven project package'){
      steps{
      	sh 'mvn package -DskipTests'
      }
    }
  }
} 
