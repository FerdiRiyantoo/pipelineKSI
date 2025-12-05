pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git branch: 'main', url: 'https://github.com/FerdiRiyantoo/pipelineKSI.git'
      }
    }
    stage('Composer Install') {
      steps {
        sh 'composer install --no-interaction --prefer-dist'
      }
    }
    stage ('run PHPUnit tests') {
      steps {
        sh './vendor/bin/phpunit tests --testdox --colors=never --no-coverage'
      }
    }
    stage ('Hello') {
      steps {
        echo 'Hello, Ferdi Riyanto!'
      }
      }
    }
  }