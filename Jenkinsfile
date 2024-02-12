pipeline {
  agent any
  stages {
    stage('CheckOut GIT') {
      steps {
        git(url: 'https://github.com/imedB1988/repo_curriculum.git', branch: 'master')
      }
    }

    stage('tools') {
      parallel {
        stage('tools') {
          steps {
            tool(name: 'nodejs', type: 'nodejs')
          }
        }

        stage('example') {
          steps {
            sh 'npm config ls'
          }
        }

      }
    }

  }
}