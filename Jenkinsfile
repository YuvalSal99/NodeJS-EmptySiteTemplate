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
        sleep 5
        sh 'npm run start &'
      }
    }

    stage('test') {
      steps {
        sh 'curl localhost:8080'
        sh 'sudo netstat -lpn |grep :\'8080\''
      }
    }

  }
}