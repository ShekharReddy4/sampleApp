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
                bat "\"${tool 'MSBuild'}\" newConsoleApp.sln /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}
            }
        }
    }
}
