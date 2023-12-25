pipeline {
  agent any
  stages {
    stage('Fetch') {
      steps {
        git(url: 'git@github.com:vijeshnair89/blue-ocean.git', branch: 'main')
      }
    }

    stage('Install') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}