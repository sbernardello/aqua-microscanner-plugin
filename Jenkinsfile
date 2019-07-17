pipeline {
  agent any


  stages {
    stage('Checkout') {
            steps {
                checkout scm
            }
    }

    stage('Build') {
      steps {
        echo "empty"
      }
    }

    stage('Package') {
      steps {
        sh '''
          mvn package -e
        '''
      }
    }
  }
}