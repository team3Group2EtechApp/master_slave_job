pipeline{
    agent{
        label {
            label 'slave1'
        }
    }
    stages{
        stage('version-control'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/team3Group2EtechApp/master_slave_job.git']]])
            }
        }
        stage('stage2'){
            steps{
                sh 'echo "abisola"'
            }
        }
        stage('stage3'){
            agent{
                label{
                    label 'slave2'
                }
            }
            steps{
                sh 'echo "Phil"'
            }
        }
        stage('stage4'){
            steps{
                sh 'echo "anthony"'
            }
        }
        stage('stage5'){
            agent{
                label{
                    label 'slave3'
                }
            }
            steps{
                sh 'echo "judith"'
            }
        }
        stage('stage6'){
            steps{
                sh 'echo "christiane"'
            }
        }
    }
}    