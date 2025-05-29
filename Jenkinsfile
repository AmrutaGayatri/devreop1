pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/AmrutaGayatri/devreop1.git', branch: 'master', credentialsId: 'aced2c8f-5e11-4521-bdda-23636cc84894')
        sh '''sudo docker build -t amrutagayatri/jrepo1:latest .
sudo docker push amrutagayatri/jrepo1:latest'''
      }
    }

    stage('Deply') {
      steps {
        sh '''sudo docker run -d -p 7777:8080 amrutagayatri/jrepo1:latest
'''
      }
    }

  }
}