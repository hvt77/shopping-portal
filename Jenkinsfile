pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        echo 'this is the compile job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/destination/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'hvt - this pipeline has completed...'
    }

  }
}