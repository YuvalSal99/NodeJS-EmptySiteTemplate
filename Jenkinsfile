pipeline {
  agent {
    node {
      label 'docker'
    }

  }
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/YuvalSal99/NodeJS-EmptySiteTemplate.git', branch: 'master')
      }
    }

    stage('build') {
      steps {
        sh 'npm install'
      }
    }

  }
}