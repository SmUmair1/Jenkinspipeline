pipeline {
  agent any
  environment {
    NEW_VERSION = '1.3.0'
  }
  stages {
    stage('build') {
      steps {
        echo 'building the app'
        echo "bulding version ${NEW_VERSION}"
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
