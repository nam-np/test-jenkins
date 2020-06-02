pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
                sh 'chmod +x test.sh'
                sh './test.sh'
            }
        }
    }

    post {
        always {
            echo 'One way or another, I have finished'
        }
        success {
            echo 'I succeeeded!'
        }
        unstable {
            echo 'I am unstable :'
        }
        failure {
            echo 'I failed'
        }
        changed {
            echo 'Things were different before...'
        }
    }
}
