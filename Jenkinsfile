pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn package'
      }
    }
    stage('Test coverage') {
      steps {
        sh 'mvn cobertura:cobertura'
        cobertura(coberturaReportFile: '**/target/site/cobertura/coverage.xml')
      }
    }
    stage('Deploy') {
      steps {
        sh '''echo "Deployment done"
'''
      }
    }
  }
}