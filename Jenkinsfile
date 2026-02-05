pipeline{
    agent any

    stages{
        stage("Restore dependencies"){
            steps{
                bat 'dotnet restore'
            }
            post{
                failure{
                    echo "Step failed"
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
}