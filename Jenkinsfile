
node () {

  stage ('Checkout') {
    steps {
      checkout scm
    }
  }

  stage('package') {
    steps {
      sh '''

        mvn package -e

      '''
    }
  }
}
