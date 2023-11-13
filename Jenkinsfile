pipeline{

    agent any 

    stages{

        stage('Continous Download') {

            steps{
                git branch: 'main', url: 'https://github.com/clemenrance/DEVOPS-PROJECT1.git'
            }
        }
        stage("Integration Testion"){

            steps{
                sh'mvn verify -DskipUnitTests'
            }
        }
        stage("Unit Testing"){

            steps{
              sh'mvn test'
            }
        }
        stage("Continouse Build"){

            steps{
                sh'mvn clean install'
            }
        }
    }
}