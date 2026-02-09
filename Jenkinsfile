pipeline {
    agent {
        label 'AGENT-1' 
    }
    options{
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    stages {
        stage('code'){
            steps {
                sh 'echo This is code'
                sh 'sleep 10
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
            deleteDir()
        }
        success {
            echo "this section run when pipeline is success"
        }
        failure {
            echo "this section run when pipeline is failed"
        }
    }
}