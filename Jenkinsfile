pipeline {
    agent {
        docker {
            image 'python:3.9' // Sử dụng image Python chính thức
            args '-v /var/run/docker.sock:/var/run/docker.sock' // Nếu cần chạy Docker bên trong agent
        }
    }
    stages {
        stage('Run Python') {
            steps {
                sh 'python --version' // Kiểm tra phiên bản Python
                sh 'pip install requests' // Cài đặt một thư viện Python ví dụ
                sh 'python -c "import requests; print(requests.get(\'https://api.github.com\').status_code)"' // Chạy code Python
            }
        }
    }
}
