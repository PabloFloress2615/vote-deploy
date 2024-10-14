node {
    def app
    
    stage('Clone repository') {
      

        checkout scm
    }

    stage('Update GIT') {
            script {
                withCredentials([usernamePassword(credentialsId: 'PabloFloress2615-github', passwordVariable: 'GIT_PASSWORD', usernameVariable: 'GIT_USERNAME')]) {
                    sh """
                        git config user.email "yourGitHubEmail@example.com"
                        git config user.name "yourGitHubUsername"
                        git add .
                        git commit -m "Automated commit by Jenkins"
                        git push https://${GIT_USERNAME}:${GIT_PASSWORD}@github.com/PabloFloress2615/vote-deploy.git HEAD:refs/heads/main
                    """
                }
    
  }
}
}
