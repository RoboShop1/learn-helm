pipeline {
    agent any

    stages {
        stage('Vault') {
            steps {
                script {
                    withVault(configuration: [disableChildPoliciesOverride: false, skipSslVerification: true, timeout: 60, vaultCredentialId: 'terraform-role', vaultUrl: 'http://172.18.0.2:8200'],vaultSecrets: [[path: 'terraform/aws/awsaccesskey', secretValues: [[vaultKey: 'access_key']]],[path: 'terraform/aws/awssecretkey', secretValues: [[vaultKey: 'secret_key']]],[path: 'terraform/aws/sshkey', secretValues: [[vaultKey: 'public_key']]]]) {
                        sh 'git pull origin main'
                        sh 'terraform init && terraform apply -var "access_key=$access_key" -var "secret_key=$secret_key" -var "public_key=$public_key" --auto-approve'
                    }
                }
            }
        }
    }
}


 def configuration = [vaultUrl: 'http://my-very-other-vault-url.com',
                         vaultCredentialId: 'my-vault-cred-id',
                         engineVersion: 1]


  def secrets = [
        [path: 'secret/testing', engineVersion: 1, secretValues: [[envVar: 'testing', vaultKey: 'value_one'],[envVar: 'testing_again', vaultKey: 'value_two']]]
     ]


  withVault([configuration: configuration, vaultSecrets: secrets]) {
















{
    admin :2019
    servers {
        metrics
    }
}

:80 {
  root * /app
  file_server
  handle_path /api/* {
    reverse_proxy backend
  }
  respond /health "OK" 200 {
    close
  }
  log {
    format json
    output stdout
  }
}

{
    admin :2019
    servers {
        metrics
    }
}

:80 {
  root * /app
  file_server
  handle_path /api/* {
    reverse_proxy backend
  }
  respond /health "OK" 200 {
    close
  }
  log {
    format json
    output stdout
  }
}














