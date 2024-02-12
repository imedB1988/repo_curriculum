pipeline {
  agent any
  stages {
    stage('CheckOut GIT') {
      steps {
        git(url: 'https://github.com/imedB1988/repo_curriculum.git', branch: 'master')
      }
    }

    stage('Log') {
      steps {
        sh ''' echo "Branch is ${env.BRANCH_NAME}..."

        withNPM(npmrcConfig:\'my-custom-npmrc\') {
            echo "Performing npm build..."
            sh \'npm install\''''
      }
    }

  }
}