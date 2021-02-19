pipeline {
  agent {
    docker {
      image 'maven:3-openjdk-11'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('Maven project test') {
      steps {
        sh 'mvn clean test'
      }
    }

    stage('Maven project package') {
      steps {
        sh 'mvn package -DskipTests'
        archiveArtifacts '**/target/*.war'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
}