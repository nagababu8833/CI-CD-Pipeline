pipeline {  
    agent agent
    stages{
        stage('build stage'){
            steps{
                sh 'mvn clean install'
            }
        }
    }
    stages {
        stage ('Test stage'){
            steps{
                sh 'mvn test'
            }
        }
    }
    stages{
        stage ('depoly to Production stage'){
            steps{
                sh 'mvn depoly'
            }
        }
    }
    post{
        always {
            echo 'pipeline is completed'
        }
        success {
            echo 'pipeline is successful'
        }
        failure {
            echo 'pipeline is failure'
        }
    }
}
