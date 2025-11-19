pipeline {
    agent any 
        stages {
            stage ("apt java 17") {
                steps{
                    sh 'sudo apt in install openjdk-17-jdk -y'
                }
                
            }

            stage ("git clone") {
                steps{
                     sh '''https://github.com/Chakry-27/spring-petclinic.git'''
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

