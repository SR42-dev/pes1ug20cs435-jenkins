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
                    sh 'cmake -C main',
                    echo 'Application built'
                }
            }
        }
        stage('Test application'){
            steps{
                script{
                    /var/jenkins_home/workspace/pes1ug20cs435/main/hello_exec
                    echo 'Application tested'
                }
            }
        }
        stage('Deploy application'){
            steps{
                script{
                    docker build -t pes1ug20cs435 .
                    docker run -d pes1ug20cs435
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