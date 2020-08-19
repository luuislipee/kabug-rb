pipeline {
    agent {
      docker {
        image 'ruby'
      }
    }
    
    stages {
        stage('build') {
            steps {
                echo 'Building or Resolve dependencies'
                sh 'bundle install'
            }
        }
        stage('test') {
            steps {
                echo 'Running regressions tests'
            }
        }
        stage('UAT') {
            steps {
                echo 'Wait for user acceptance'
                input(message: 'Go to production?', ok: 'Yes')
            }
        }
        stage('Prod') {
            steps {
                echo 'WebApp is ready! :)'
            }
        }
    }
}