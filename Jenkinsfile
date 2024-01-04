pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'git@github.com:vijeshnair89/blue-ocean.git', branch: 'main')
      }
    }

    stage('Install apache') {
      steps {
        sh '''sudo apt-get update -y
sudo apt-get install apache2 -y'''
      }
    }

    stage('Deploy') {
      steps {
        sh '''sudo cp -R * /var/www/html/
sudo systemctl restart apache2'''
      }
    }

  }
}