pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('SAST') {
            steps {
                sh "curl  -X POST -d 'auth='${auth}'&langType=php&projectName=dvwa&downloadType=2&svngitUrl='${svngitUrl}'&svngitUserName='${svngitUserName}'&svngitPassword='${svngitPassword}'&projectGroupName='${projectGroupName} $checkUrl/cp4/webInterface/postSourceCodeBySvnGit.action"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
