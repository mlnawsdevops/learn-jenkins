pipeline {
    agent {
        label 'AGENT-1'
    }
    stages {
        stage('code'){
            steps {
                sh 'echo This is code'
            }
        }
        stage('build'){
            steps{
                sh 'echo This is build'
            }
        }
        stage('test'){
            steps{
                sh 'echo This is test'
            }
        }
        stage('deploy'){
            steps{
                sh 'echo This is deploy'
            }
        }
    }

    post {
        always {
            echo "this sections run always"
        }
        success {
            echo "this section run when pipeline is success"
        }
        failure {
            echo "this section run when pipeline is failed"
        }
    }
}