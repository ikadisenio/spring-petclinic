#!groovy
pipeline {
	agent any
	stages {
		stage('Maven Install') {
			agent any
			steps {
				sh 'mvn clean install'
			}
		}
		stage('Docker Build') {
			agent any
			steps {
				sh 'docker build -t grupo03/spring-petclinic:latest .'
			}
		}
	}
}
