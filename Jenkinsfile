pipeline {
    agent { label 'node2' }

    options {
        timeout(time: 15, unit: 'MINUTES')
    }

    triggers {
        pollSCM('H */4 * * 1-5')
    }

    tools {
        jdk 'JDK_17'
    }

    stages {

        stage('GIT cloning') {
            steps {
                git url: 'https://github.com/muthyalasaikiran/spring-petclinic.git',
                    branch: 'main'
            }
        }

        stage('Build and Package') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Reporting') {
            steps {
                archiveArtifacts artifacts: '**/target/spring-petclinic-*.jar'
                junit '**/target/surefire-reports/TEST-*.xml'
            }
        }
    }
}
