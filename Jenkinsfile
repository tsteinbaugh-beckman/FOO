pipeline {
    agent any
    
    stages {
        stage ('hello') {
            steps {
                script {
                    echo "${env.CHANGE_ID}"
                }
            }
        }
    }
}
