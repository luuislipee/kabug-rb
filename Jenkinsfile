pipeline {
    agent {
      docker {
        image 'chiaradialuis/rubywd'
      }
    }
    
    stages {
        stage('build') {
            steps {
                echo 'Building or Resolve dependencies'
                sh 'rm -f Gemfile.lock'
                sh 'bundle install'
            }
        }
        stage('test') {
            steps {
                echo 'Running regressions tests'
                sh 'bundle exec cucumber -p ci'
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