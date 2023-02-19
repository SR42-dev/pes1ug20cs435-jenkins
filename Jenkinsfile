pipeline{
    agent any
    stages{
        stage('Build application'){
            steps{
                script{
                    make -C main,
                    echo 'Application built'
                }
            }
        }
        stage('Test application'){
            steps{
                script{
                    ./main/hello_exec,
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