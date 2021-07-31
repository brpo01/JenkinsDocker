pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building Application'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing Application'
            echo '"This is Jenkins project path- ${JenkinsDocumentPath}"'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying Application'
      }
    }

  }
  environment {
    JenkinsDocumentPath = '"C:\\Users\\Praise\\Documents\\jenkins-projects"'
  }
}