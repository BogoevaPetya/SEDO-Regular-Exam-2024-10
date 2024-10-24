pipeline {
    agent any

    environment{
        CHROME_VERSION = '127.0.6533.73'
        CHROMEDRIVER_VERSION = '127.0.6533.73'
        CROME_INSTALL_PATH = 'C:\\Program Files\\Google\\Chrome\\Application'
        CHROMEDRIVER_PATH = 'C:\\Program Files\\Google\\Chrome\\Application\\chromedriver.exe'
    }
    stages {
        stage(Restore dependencies') {
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Dotnet build') {
            steps {
                bat 'dotnet build'
            }
        }
        stage('Execute tests') {
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }     
    }
}
