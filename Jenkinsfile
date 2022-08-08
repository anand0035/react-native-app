pipeline{
    agent any
    environment {
            //Fastlane Environment Variables

           APP_NAME = "DEMO_APP"
            LC_ALL = "en_US.UTF-8"
            LANG = "en_US.UTF-8"

        }

    stages
    {
//         stage('npm install'){
//             steps{
//                 bat 'npm install'
//             }
//         }
//         stage('testing your code'){
//             steps{
//                 bat 'npm run test'
//             }
//         }
        stage('build android'){
            steps{
//                  bat 'icacls "android/gradlew" /grant Users:F'
                sh "chmod +x android/gradlew"
                sh "Fastlane android build"
            }
        }
    }
}

