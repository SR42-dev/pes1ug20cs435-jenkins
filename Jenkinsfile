pipeline{
    agent any
    stages{
        stage('Clone repository'){
            steps{
                git branch: 'main',
                url: 'https://github.com/SR42-dev/pes1ug20cs435-jenkins'
            }
        }
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
                    ./hello_exec
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