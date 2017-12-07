#!/usr/bin/env groovy//
properties([
    [$class: 'GithubProjectProperty',
    displayName: '',
    projectUrlStr: 'https://github.com/MyFirstOrgProj/Repo2.git/'],
    pipelineTriggers([upstream(
   threshold: 'SUCCESS',
   upstreamProjects: 'https://github.com/MyFirstOrgProj/Repo1.git'
   )])])

pipeline {
    agent any 

    stages {
        stage('Build') { 
            steps { 
                sh 'pwd' 
            }
        }
        stage('Test'){
            steps {
                sh 'java -version'
                
            }
        }
        stage('Deploy') {
            steps {
                sh 'ls'
                sh 'pwd'
            }
        }
    }
}
