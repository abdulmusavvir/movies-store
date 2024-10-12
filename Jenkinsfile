pipeline{
    stages{
        stage("checkout"){
            steps{
                git branch: 'develop',
                credentialsId: '1d192c85-7a4a-4494-b009-d9ac77c3a8ec', 
                url: 'https://github.com/abdulmusavvir/movies-store.git'
            }
            post{
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }
    }
    post{
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
