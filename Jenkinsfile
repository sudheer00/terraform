pipeline {
    agent any
    stages {
        stage("OS version"){
            steps {
                echo "Terraform version"
                sh " terraform version"
            }
        }
        stage ("terraform initialization") {
          steps {
            sh "terraform init"
          }
        }
        stage ("Deploy") {
            steps {
          echo "Selected option is --> ${action}"
          sh "terraform ${action}  --auto-approve"
                }
        }        
    }
}
