pipeline {
  agent any
  options { timestamps() }
  stages {
    stage('Checkout') {
      steps { checkout scm }
    }
    stage('Build') {
      steps { sh 'mvn clean package -DskipTests=false' }
    }
    stage('Unit Test') {
      steps { sh 'mvn test' }
    }
    stage('Static Check') {
      steps { sh 'echo SonarQube or static scan goes here' }
    }
  }
}
