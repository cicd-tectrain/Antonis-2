pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
        //currentBuild.result = FAILURE
      }
    }

    stage('Deploy') {
      when {
        branch 'feature/*'
        beforeAgent true
      }

      steps {
        echo 'Deploying'
      }
    }

  }
}