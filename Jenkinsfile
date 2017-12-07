pipeline {
    agent none
    stages {
        stage('Build') { 
            steps { 
              bat 'dir' 
            }
        }
        stage('Test'){
            steps {
              bat 'ipconfig'
            }
        }
        stage('Deploy') {
            steps {
                powershell '''
                dir
                '''
            }
        }
        stage('Deployment') {
            steps {
                bat "\"${tool 'MSBuild'}\" newConsoleApp.sln
            }
        }
    }
}
