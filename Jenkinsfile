pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/vijeshnair89/blue-ocean.git', branch: 'main')
      }
    }

    stage('Install apache') {
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