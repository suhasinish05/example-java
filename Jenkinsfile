pipeline{
    agent {label 'sonar'}
    stages{     
       stage('Build Stage'){
            steps{
                sh 'mvn clean install'
            }
         }
       stage('deploy stage') {
            agent {
                label 'tomcat'
            }
            steps{
                script {
                  sh 'curl -o  http://13.235.241.137:8081/artifactory/libs-release/com/example/jenkins-test/1.1/jenkins-test-1.1.jar'
                  
                }
            }
        }
    }
}
