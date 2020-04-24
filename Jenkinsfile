pipeline {
agent any
	stages{
			stage('Compile Stage'){
				steps{
					withMaven(maven : 'apache-maven-3.6.3'){
						sh 'mvn clean compile'
					}
				}
			}
			stage('Deployment Stage'){
				steps{
					withMaven(maven : 'apache-maven-3.6.3'){
						sh 'mvn deploy'
					}
				}
			}
	}

}
