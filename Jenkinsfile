pipeline {
    agent any 
        stages {

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

