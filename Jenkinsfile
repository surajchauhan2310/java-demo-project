pipeline {
  agent any

  stages {
    stage('01.Clone Repo') {
      steps {
       git branch: 'master', credentialsId: 'demo', url: 'https://github.com/surajchauhan2310/java-demo-project'
      }
    }
    stage('02.Clean') {
      steps {
        bat 'mvn clean'
      }
    }
    stage('03.Package') {
      steps {
       bat 'mvn package'
      }
    }
  }
}
