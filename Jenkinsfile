timestamps {
    node () {
        stage ('Checkout') {
            withCredentials([
                conjurSecretCredential(credentialsId: 'DB_USERNAME', variable: 'DB_LOGIN'),
                conjurSecretCredential(credentialsId: 'DB_PASSWORD', variable: 'DB_PASS')
            ]) {
                sh '''
                    echo "Postgres username: $DB_LOGIN"
                    echo "Postgres password: $DB_PASS"
                '''
            }
        }
    }
}