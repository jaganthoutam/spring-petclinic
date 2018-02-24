#!groovy

pipeline {
  agent none
  stages {
    stage('Maven Install') {
      agent {
        docker {
          image 'maven:3.5.0'
        }
      }
      steps {
        sh 'mvn clean install'
      }
    } 
stage('Docker build') {
 agent any
 step {
  sh 'docker build -t shanem/spring-petclinic:latest .'
      }
    }
  }
}
