#!/usr/bin/env groovy

node ('master'){
    stage('Build and Test') {
        properties([pipelineTriggers([[$class: 'GitHubPushTrigger']])])
        git branch: 'https://github.com/sharb/webapp',
             url: 'ssh://git@bitbucket.org:company/repo.git'
        env.PATH = "${tool 'Maven 3'}/bin:${env.PATH}"
        sh 'mvn clean package'
    }
}
