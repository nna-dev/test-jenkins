pipeline {
    agent {
        docker { image 'jenkins/jnlp-agent-python3' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'python --version'
                sh 'pytest ./'
            }
        }
    }
}
