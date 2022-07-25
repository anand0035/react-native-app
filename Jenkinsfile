pipeline{
    agent any

    stages
    {
        stage('npm install'){
            steps{
                bat 'npm install'
            }
        }
        stage('testing your code'){
            steps{
                bat 'npm run test'
            }
        }
        stage('build android'){
            steps{
                bat 'fastlane build android'
            }
        }
    }
}

