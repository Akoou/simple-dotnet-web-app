pipeline {
  agent any
  stages {
    stage('Restore') {
      steps {
        dotnetRestore()
      }
    }

    stage('Build') {
      steps {
        dotnetBuild(configuration: 'Release')
      }
    }

    stage('Test') {
      steps {
        dotnetTest()
      }
    }

    stage('Publish') {
      steps {
        dotnetPublish(outputDirectory: 'publish', configuration: 'Release')
      }
    }

    stage('Deploy') {
      steps {
        echo 'echo "Deploying to server..."'
      }
    }

  }
}