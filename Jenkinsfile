pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'building the app'
      }
    }
    
    stage('test') {
      when {
        expression {
          BRANCH_NAME == 'master'
        }
      }
      steps {
        echo 'testing the app'
      }
    }
    
    stage('deploy') {
      steps {
        echo 'deploying the app'
      }
    }
  }
}
