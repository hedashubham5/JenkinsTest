pipeline {
    agent any
    stages {
        stage("Intialize Pipeline"){
            steps {
                script {
                    echo "Intitialize pipeline: ${Data}"
                    sh ls
                    sh pwd
                    if (env.BRANCH == 'master') {
                        echo "Master Branch"
                    } else {
                        echo "Unknown Branch"
                    }
                }
            }
        }
    }
}