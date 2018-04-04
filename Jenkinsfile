#!/usr/bin/env groovy

node ('master'){
    stage('Set Trigger') {
        properties([pipelineTriggers([[$class: 'GitHubPushTrigger']])])
        git url: 'https://github.com/sharb/webapp.git', branch: 'master'
    }
    stage('build'){
        echo 'build'   
    }
}
