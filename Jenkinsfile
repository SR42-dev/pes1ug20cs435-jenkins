pipeline{
    agent any
    stages{
        stage('Build application'){
            steps{
                sh 'make -C main'
                    
            }
        }
        stage('Test application'){
            steps{
                    sh './main/hello_exec'
            }
        }
        stage('Deploy application'){
            steps{
                echo 'Application deployed'
            }   
        }
    }
    post{
        failure{
            echo 'Pipeline failed'
        }
    }
}