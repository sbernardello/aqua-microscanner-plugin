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

  post {
        //always {
        //    deleteDir() /* clean up our workspace */
            /* 
                Can clean docker images built
                docker image prune -a --force --filter "until=240h" 
            */
            
        //}
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}