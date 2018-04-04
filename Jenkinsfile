#!/usr/bin/env groovy

node ('master'){
    stage('Build and Test') {
        properties([pipelineTriggers([[$class: 'GitHubPushTrigger']])])
        git url: 'https://github.com/sharb/webapp.git', branch: 'master'
        sh 'mvn clean package'
    }
}
