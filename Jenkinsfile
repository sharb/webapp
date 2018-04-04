#!/usr/bin/env groovy

node ('master'){
    stage('Set Trigger') {
        properties([pipelineTriggers([[$class: 'GitHubPushTrigger']])])
        git url: 'https://github.com/sharb/hook-test.git', branch: 'master'
    }
    stage('build'){
        sh 'cat README.md'   
    }
}
