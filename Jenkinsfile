node
{
   
    stage("SCM Checkout")
    {
        git url: 'https://github.com/FIROZBAHA/Recent.git'
    }
    stage("Maveen Build")
    {
       def mvnHome = tool name: 'Maveen', type: 'maven'
       env.JAVA_HOME = tool name: 'JDK', type: 'jdk'
       bat "\"${mvnHome}\"\\bin\\mvn -B verify"
            }
      stage('Archiving Artifacts')
            {
            archiveArtifacts artifacts: "target/*.jar", onlyIfSuccessful: true
               
            }
    }
