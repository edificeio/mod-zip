#!/usr/bin/env groovy

pipeline {
  agent any
    stages {
      stage("Initialization") {
        steps {
          buildName "${GIT_BRANCH}"
        }
      }
      stage('Build') {
        steps {
          checkout scm
          sh './build.sh init clean install publish'
        }
      }
    }
}

