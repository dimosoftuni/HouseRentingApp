pipeline{
    agent any

    stages{
        stage("Restore dependencies"){
            steps{
                bat 'dotnet restore'
            }
            post{
                always{
                    echo "Step executed successfully"
                }
            }
        }

        stage("Build solution"){
            steps{
                bat 'dotnet build'
            }
        }

        stage("Run tests"){
            steps{
                bat 'dotnet test'
            }
        }
    }

    post{
        always{
            echo "Workflow completed successfully"
        }
}