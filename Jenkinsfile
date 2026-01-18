pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "✅ Code checkout done from GitHub SCM"
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Info') {
            steps {
                sh 'echo "Branch: $(git rev-parse --abbrev-ref HEAD)"'
                sh 'echo "Last commit:"'
                sh 'git log -1 --oneline'
            }
        }

        stage('Success') {
            steps {
                echo "✅ Episode 9 pipeline executed successfully!"
            }
        }
stage('Intentional Fail') {
    steps {
        sh 'echo "Failing on purpose for Episode 10"'
        sh 'exit 1'
    }
}

    }

    post {
        success {
            echo "🎉 Pipeline SUCCESS"
        }
        failure {
            echo "❌ Pipeline FAILED"
        }
    }
}
