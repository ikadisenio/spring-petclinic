#!groovy
pipeline {
    agent none // Agent is defined per stage
    stages {
        stage('Maven Install') {
            agent {
                docker {
                    image 'maven:3.5.0'
                }
            }
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Docker Build') {
            agent any // This stage runs on the main Jenkins agent
            steps {
                sh 'docker build -t grupo03/spring-petclinic:latest .'
            }
        }
    }
}
