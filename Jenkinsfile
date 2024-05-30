pipeline {  
    agent any
    stages{
        stage('build stage'){
            steps{
                sh 'mvn clean install'
            }
        }
    }

        stage ('Test stage'){
            steps{
                sh 'mvn test'
            }
        
    }
   
        when{
            branch 'master'
        }
        stage ('depoly to Production stage'){
            steps{
                sh 'mvn depoly'
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
