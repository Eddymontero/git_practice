pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/Eddymontero/git_practice', branch: 'main')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End unit test') {
          steps {
            sh 'cd curriculum-front && npm i && npm run test:unit '
          }
        }

      }
    }

  }
}