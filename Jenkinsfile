pipeline {
    agent {
        label "jenkins-maven"
    }
    
    environment {
      JAVA_OPTIONS="-Xms1024m -Xmx1048m"
    }
    
    stages{
        stage('Test Memory'){
            steps{
                sh 'java -XX:+PrintFlagsFinal -version | grep HeapSize'
                
                sh 'mvn clean package'
            }
        }
    }
}
