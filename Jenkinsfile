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
    JenikinsDocumentPath = '"C:\\Users\\Praise\\Documents\\jenkins-projects"'
  }
}