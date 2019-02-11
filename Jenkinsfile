

pipeline {

  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
      post {
        success {
          echo 'Now, archiveing artifacts...'
          archiveArtifacts artifacts '**/target/*.war'
        }
      }
    }
  }

}



