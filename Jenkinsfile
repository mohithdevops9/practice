pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the Git repository
                checkout scm
            }
        }
        
        stage('Build and Test') {
            steps {
                // Add your build and test steps here
                sh 'echo " running "'
            }
        }
        
        stage('Push to Git') {
            steps {
                script {
                    // Set up Git configuration (if needed)
                    sh 'git config user.email "mohithdevops9@gmail.com"'
                    sh 'git config user.name "mohithdevops9"'
                    
                    // Commit and push changes
                    sh 'echo "Hi" > newfile'
                    sh 'git add newfile'
                    sh 'git commit -m "added from jenkins file :Jenkins build: ${BUILD_NUMBER}"'
                    //sh 'git checkout -b main'
                    sh 'gitPush()'  // Modify branch name as needed
                }
            }
        }
    }
}
