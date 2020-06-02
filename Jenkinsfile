pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
                echo '===================== Install dependencies ====================='
                sh 'npm i'
                sh 'ls'
                sh 'node_modules/.bin/cypress run  --reporter junit -s cypress/integration/sw360/homepage/login.spec.js'
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
