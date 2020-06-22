#!groovy

pipeline {
  agent any
  stages{
    stage('') {
      agent any
      when {
        anyOf {
          branch 'dev'
          branch 'master'
        }
      }
      steps {
        
      }
    }
    stage('') {
      agent any
      when {
        anyOf {
          branch 'dev'
        }
      }
      steps {
        
      }
    }
  }
  post {
    always {
      deleteDir()
    }
  }
}
