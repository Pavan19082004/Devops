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

        stage('Intentional Fail') {
    steps {
        sh 'echo "Failing on purpose for Episode 10"'
        sh 'exit 1'
    }
}


        stage('Success') {
            steps {
                echo "✅ Episode 9 pipeline executed successfully!"
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
