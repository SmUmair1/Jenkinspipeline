pipeline {
  agent any

  //here i'm using my own enviromental variable We can also check enviromental variable by localhost:8080/env-vars.html/
  environment {
    NEW_VERSION = '1.3.0'
  }
  stages {
    stage('build') {
      steps {
        echo 'building the app'
  //here I'm using enviromental variable but not using in the double qoute 
        echo "bulding version ${NEW_VERSION}"
      }
    }
    
    stage('test') {
      // here I'm giving condition that whether the branch is master or dev or any else. If the branch is master then it will excute this stage or it missed.
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
