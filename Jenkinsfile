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
            echo "This is Jenkins project path- ${JenkinsDocumentPath}"
          }
        }

        stage('Test Txt') {
          steps {
            writeFile(file: 'text.txt', text: 'This is a test file')
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            echo 'Deploying Application'
            input(message: 'Should Deployment run??', id: 'Ok')
          }
        }

        stage('Artifact') {
          steps {
            archiveArtifacts 'text.txt'
          }
        }

      }
    }

  }
  environment {
    JenkinsDocumentPath = '"C:\\Users\\Praise\\Documents\\jenkins-projects"'
  }
}