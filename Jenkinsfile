pipeline {
  agent any

  triggers {
    githubPush()  // This listens for GitHub push events
  }
<<<<<<< HEAD
//testing the webhooks again.
//testing the webhooks again2.
  //testing the webhooks again3.
=======

>>>>>>> e7a7dc2 (adding the java run steps into the Jenkinsfile)
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
    stage('04.Run Application') {
      steps {
        script {
          // Use Maven to run the application instead of manually invoking the JAR
          sh 'mvn spring-boot:run'
        }
      }
    }
  }
}
