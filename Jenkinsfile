#!/usr/bin/env groovy

node ('master'){
    stage('Build and Test') {
        properties([pipelineTriggers([[$class: 'GitHubPushTrigger']])])
        git url: 'https://github.com/someone/something.git', branch: 'master'
        sh 'mvn clean package'
    }
}
