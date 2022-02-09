pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'build completed'
        retry(count: 3) {
          echo 'trying to build'
          sh 'wwwwww'
        }

      }
    }

    stage('test stages') {
      parallel {
        stage('test stages') {
          steps {
            echo 'run test2'
          }
        }

        stage('test1') {
          steps {
            echo 'running test1'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        input(message: 'are you sure to deploy', ok: 'yes i sure')
        echo 'test deploy'
      }
    }

    stage('notify for new build') {
      steps {
        echo 'new build'
      }
    }

  }
}