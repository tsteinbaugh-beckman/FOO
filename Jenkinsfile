pipeline {
    agent any
    
    stages {
        stage ('hello') {
            steps {
                echo 'hello'
            }
        }
        stage ('build next foo2') {
            steps {
                script {
                    if (expression {return "test/foo2/${env.BRANCH_NAME}"}) {
                        echo "test/foo2/${env.BRANCH_NAME}"
                        echo return "test/foo2/${env.BRANCH_NAME}"
                        build job: "test/foo2/${env.BRANCH_NAME}", propagate: false, wait: false
                    }
                    else {
                        build job: 'test/foo2/main', propagate: false, wait: false
                    }
                }
            }
        }
    }
}    
