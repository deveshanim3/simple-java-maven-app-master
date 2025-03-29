pipeline{
    agent any
    tools{
        maven 'maven'
    }
    stages{
        stage('Build'){
            steps{
                bat 'mvn clean package'
            }
        }
        stage('Test'){
            steps{
                bat 'mvn test'
            }
        }
        stage('Run'){
            steps{
                script{
                    def output=bat(script: 'java -jar target/my-app-1.0-SNAPSHOT.jar', returnStdout: true).trim())
                    echo "Output from java: ${output}"
                }
            }
        }
    }
}














