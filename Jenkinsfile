pipeline {
    agent any 
        stages {

            stage ("git clone") {
                steps{
                   git url: 'https://github.com/Chakry-27/spring-petclinic.git',    
                      branch: "main"
                }
               
            }

            stage ("mvn install") {
                steps{
                    sh 'sudo apt install maven'
                }
                
            }

            stage ("mvn package") {
                steps{
                    sh 'mvn package'
                }
                
            }
            stage ("mvn --version") {
                steps{
                    sh '''mvn --version java -version'''
                }
                  

            }
        }
}

