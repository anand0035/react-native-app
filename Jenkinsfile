pipeline{
    agent any
    environment {
            // Fastlane Environment Variables
            PATH = "C:/Ruby31-x64/lib/ruby/gems/3.1.0/gems/fastlane-2.208.0/bin" +
                    "$HOME/.rvm/gems/ruby-2.5.3/bin:" +
                    "$HOME/.rvm/gems/ruby-2.5.3@global/bin:" +
                    "$HOME/.rvm/rubies/ruby-2.5.3/bin:" +
                    "/usr/local/bin:" +
                    "$PATH"
            LC_ALL = "en_US.UTF-8"
            LANG = "en_US.UTF-8"

        }

    stages
    {
        stage('npm install'){
            steps{
                bat 'npm install'
            }
        }
//         stage('testing your code'){
//             steps{
//                 bat 'npm run test'
//             }
//         }
        stage('build android'){
            steps{
                bat 'fastlane build android'
            }
        }
    }
}

