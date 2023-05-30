pipeline {
  agent {
    node {
      label 'node16'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh '''node -v
npm -v
ng --version'''
        cleanWs(cleanWhenAborted: true, cleanWhenFailure: true, cleanWhenNotBuilt: true, cleanWhenSuccess: true, cleanWhenUnstable: true, cleanupMatrixParent: true, deleteDirs: true)
      }
    }

  }
}