pipeline {
  agent any

  triggers {
   githubPush()  // This listens for GitHub push events and trying to impelment the webhooks into it
  }
//testing the webhooks
  stages {
    stage('01.Clone Repo') {
      steps {
        git branch: 'master', credentialsId: 'demo', url: 'https://github.com/surajchauhan2310/java-demo-project'
      }
    }
    stage('02.Clean') {
      steps {
        sh 'mvn clean'
      }
    }
    stage('03.Package') {
      steps {
        sh 'mvn package'
      }
    }
  }
}
