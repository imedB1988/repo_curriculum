pipeline {
  agent any
  stages {
    stage('CheckOut GIT') {
      steps {
        git(url: 'https://github.com/imedB1988/repo_curriculum.git', branch: 'master')
      }
    }

    stage('installl dependencies') {
      parallel {
        stage('installl dependencies') {
          steps {
            sh 'npm install'
          }
        }

        stage('NPM Test') {
          steps {
            sh 'npm test'
          }
        }

      }
    }

  }
}