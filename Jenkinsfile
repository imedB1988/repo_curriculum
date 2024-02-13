pipeline {
  agent any
  stages {
    stage('CheckOut GIT') {
      steps {
        git(url: 'https://github.com/imedB1988/repo_curriculum.git', branch: 'master')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh 'ls -al'
          }
        }

        stage('Front-End Unit test ') {
          steps {
            sh 'cd curriculum-front && npm  init  && npm run test:unit'
          }
        }

      }
    }

  }
}