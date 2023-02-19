pipeline{
    agent any
    stages{
        stage('Build application'){
            steps{
                    sh 'make',
                    echo 'Application built'
            }
        }
        stage('Test application'){
            steps{
                    sh './hello_exec'
                    echo 'Application tested'
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