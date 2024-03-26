pipeline {
    agent any

    stages {
        stage('Download Batch Script') {
            steps {
                script {
                    sh "curl https://raw.githubusercontent.com/Tybcsy71/hw_devops_39_tibor_szente_jenkins/main/install_apache.sh > ./install_apache.sh"
                    sh "chmod +x install_apache.sh "
                    sh "bash -c 'sudo ./install_apache.sh'"
                    archiveArtifacts artifacts: 'apache_install_date.txt'
                }
            }
        }
    }
}