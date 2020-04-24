pipeline {
agent any
	stages{
			stage('Compile Stage'){
				steps{
					withMaven(maven : 'apache-maven-3.6.3'){
						sh 'mvn package'
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
