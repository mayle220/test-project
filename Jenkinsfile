pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/mayle220/test-project', branch: 'main')
      }
    }

    stage('List') {
      parallel {
        stage('List') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Run tests') {
          steps {
            sh 'npm i && npm run test:dev'
          }
        }

      }
    }

  }
}