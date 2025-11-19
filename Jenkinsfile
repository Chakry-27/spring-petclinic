pipeline {
    agent any 
        steps {
            stage ("apt java 17") {
                sh 'sudo apt in install openjdk-17-jdk -y'
            }

            stage ("git clone") {
                sh '''https://github.com/Chakry-27/spring-petclinic.git'''
            }

            stage ("mvn install") {
                sh 'sudo apt install maven'
            }

            stage ("mvn package") {
                sh 'mvn package'
            }
            stage ("mvn --version") {
                  sh '''mvn --version java -version'''

            }
        }
}

