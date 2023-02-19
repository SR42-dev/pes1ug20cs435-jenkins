pipeline{
    agent any
    stages{
        stage('Build application'){
            steps{
                script{
                    sh 'make',
                    echo 'Application built'
                }
            }
        }
        stage('Test application'){
            steps{
                script{
                    sh './hello_exec'
                    echo 'Application tested'
                }
            }
        }
        stage('Deploy application'){
            steps{
                script{
                    echo 'Application deployed'
                }
            }   
        }
    }
    post{
        failure{
            echo 'Pipeline failed'
        }
    }
}