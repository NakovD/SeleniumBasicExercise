pipeline{
    agent any
    stages{
        stage('Restore'){
            steps{
                bat 'dotnet restore'
            }
        }
        stage('Build'){
            steps{
                bat 'dotnet build --no-restore'
            }
        }
        stage('Run Project1 tests') {
            steps {
                echo 'Running tests for Project1...'
                sh 'dotnet test TestProject1/TestProject1.csproj --verbosity minimal'
            }
        }

        stage('Run Project2 tests') {
            steps {
                echo 'Running tests for Project2...'
                sh 'dotnet test TestProject2/TestProject2.csproj --verbosity minimal'
            }
        }

        stage('Run Project3 tests') {
            steps {
                echo 'Running tests for Project3...'
                sh 'dotnet test TestProject3/TestProject3.csproj --verbosity minimal'
            }
        }
    }
}