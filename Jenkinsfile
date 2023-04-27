timestamps {
    node () {
        stage ('Checkout') {
            withCredentials([
                conjurSecretCredential(credentialsId: 'GITHUB_USERNAME', variable: 'GH_LOGIN'),
                conjurSecretCredential(credentialsId: 'GITHUB_PASSWORD', variable: 'GH_PASS')
            ]) {
                sh '''
                    echo "GitHub login: $GH_LOGIN"
                    echo "GitHub pass: $GH_PASS"
                '''
            }
        }
    }
}