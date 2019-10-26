pipeline {
    agent any
    stages {
        stage("Intialize Pipeline"){
            steps {
                script {
                    echo "Intitialize pipeline: ${Data}"
                    sh "ansible-playbook -i inventory -e password=${password} -e user=${user} main.yaml"
                    if (env.BRANCH == 'master') {
                        echo "Master Branch ${NODE_NAME}"
                    } else {
                        echo "Unknown Branch ${NODE_NAME}"
                    }
                }
            }
        }
    }
}