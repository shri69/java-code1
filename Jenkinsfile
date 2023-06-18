pipeline{
    agent any
    stages{
        stage("Checkout the code"){
            steps{
                sh 'git clone https://github.com/Ramkhushi/java-code1.git'
            }
            
        }
        stage('mvn compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('mvn test'){
            steps {
                sh 'mvn test'
            }
        }
        stage('mvn package'){
            steps {
             sh 'mvn package'
            }
            
        }

    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}