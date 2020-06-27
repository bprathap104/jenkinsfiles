pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo \'ready\''
      }
    }

    stage('test') {
      steps {
        echo 'this is a testing stage'
      }
    }

    stage('deploy') {
      steps {
        sh '''#!/bin/bash
echo `pwd` > pipeline.log
'''
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts 'pipeline.log'
      }
    }

  }
}