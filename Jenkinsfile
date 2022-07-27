pipeline{
    agent any
    environment {
            // Fastlane Environment Variables
            PATH = "$HOME/.fastlane/bin:" +
                    "$HOME/.rvm/gems/ruby-2.5.3/bin:" +
                    "$HOME/.rvm/gems/ruby-2.5.3@global/bin:" +
                    "$HOME/.rvm/rubies/ruby-2.5.3/bin:" +
                    "/usr/local/bin:" +
                    "$PATH"
            LC_ALL = "en_US.UTF-8"
            LANG = "en_US.UTF-8"
            VERSION_NAME = ""
            VERSION_SUFFIX = ""
            APP_VERSION_NAME = ""
            VERSION_CODE = ""
            DROPBOX_FOLDER = ""
            PROGUARD_ENABLED = ""
            JIRA_PROJECT_KEY = ""
            PROJECT_NAME = env.JOB_NAME.tokenize("/").first().replaceAll(" Android", "")
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

