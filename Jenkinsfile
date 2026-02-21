// build the application and execute all of the tests when changes are pushed to the main branch.

pipeline{

    agent any

    stages{
        stage('Restore dependencies'){
            when {
                branch 'main'
            }
            steps{
                bat 'dotnet restore'
            }
            
        }
        stage('Build application'){
            when {
                branch 'main'
            }
            steps{
                bat 'dotnet build --no-restore'
            }
            
        }
        stage('Run tests'){
            when {
                branch 'main'
            }
            steps{
                bat 'dotnet test --no-restore'
            }
            
        }
    }
    
}