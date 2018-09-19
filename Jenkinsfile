pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile.build'
    }

  }
  stages {
    stage('Docker Build') {
      steps {
        sh '''docker build -t myproject/api -f Dockerfile .
'''
      }
    }
  }
  environment {
    VAULT_ADDR = 'null'
    VAULT_TOKEN = 'null'
  }
}