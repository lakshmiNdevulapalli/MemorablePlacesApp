pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'gradle tasks'
        slackSend(baseUrl: 'https://hooks.slack.com/services/', channel: '#alerts', color: 'Green', message: "SUCCESSFUL: JOB \'${env.JOB_NAME} [${env.BUILD_NUMBER}]\' (${env.BUILD_URL})")
      }
    }
  }
}