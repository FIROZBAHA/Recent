pipeline {
agent any
	stages{
			stage('Compile Stage'){
				steps{
					withMaven(maven : 'apache-maven-3.6.3'){
						sh 'mvn clean install'
					}
				}
			}
			stage('Deployment Stage'){
				def myhome = tool name: 'apache-maven-3.6.3', type: 'maven'
				sh "${myhome}/bin/mvn package"
			}
	}

}
