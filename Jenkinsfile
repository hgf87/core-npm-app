pipeline {
  agent {
    kubernetes {
      label 'mypodtemplate-npm-6'
      defaultContainer 'node-container'
      yamlFile 'KubernetesPod.yaml'
    }
  }
  stages {
    stage('Build Node 10') {
      steps {
        container('node-10-container') {
          sh 'npm install'
        }
      }
    }
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
  }
}
