pipeline {
  agent {
    node {
      label 'iac'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        checkout(scm: [$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/teammira2023/izac2.git']]], changelog: true, poll: true)
      }
    }

    stage('IAC Code Quality Check') {
      steps {
        sh '''sonar-scanner \\
  -Dsonar.projectKey=izac \\
  -Dsonar.sources=. \\
  -Dsonar.host.url=http://34.202.247.19:9000 \\
  -Dsonar.login=sqp_9eb7212aa3afce8cb1ef705bbba2e55b626888a3'''
      }
    }

    stage('Environment Build - init') {
      steps {
        sh 'chmod +x disa.sh'
        sh 'chmod +x mya.sh'
        sh 'chmod +x mytina.sh'
        sh './mya.sh'
      }
    }

    stage('terraform validate') {
      steps {
        sh './disa.sh'
      }
    }

    stage('terraform in Action') {
      steps {
        sh 'echo $AWS_ACCESS_KEY_ID'
        sh 'echo $AWS_SECRET_ACCESS_KEY'
        sh 'echo $AWS_SESSION_TOKEN'
        sh './mytina.sh'
      }
    }

  }
}
