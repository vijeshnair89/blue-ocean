pipeline {
  agent any
  stages {
    stage('fetch') {
      steps {
        git(url: 'git@github.com:vijeshnair89/blue-ocean.git', branch: 'main')
      }
    }

    stage('install') {
      steps {
        sh 'sudo apt-get install apache2 -y'
      }
    }

    stage('deploy') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}