pipeline {
    agent {
        label "jenkins-maven"
    }
    
    environment {
      MAVEN_OPTS="-Xms1024m -Xmx10480m"
    }
    
    stages{
        stage('Test Memory'){
            steps{
                sh 'java -XX:+PrintFlagsFinal -version | grep HeapSize'
                
                container('maven'){
                    sh 'mvn clean package'
                }
            }
        }
    }
}
