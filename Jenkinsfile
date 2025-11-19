pipeline {
    agent any 
        stages {
            tools {
                maven 'Maven-3.8.6' , jdk 'JDK-17'
            }


            stage ("git clone") {
                steps{
                   git url: 'https://github.com/Chakry-27/spring-petclinic.git',    
                      branch: "main"
                }
               
            }

            stage ("mvn package") {
                steps{
                    sh 'mvn package'
                }
                
            }
        }
}

