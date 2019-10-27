pipeline {
    agent any
    stages {
        stage("Intialize Pipeline"){
            steps {
                script {
                    echo "Intitialize pipeline: ${Data}"
                    sh "echo '${Info}' > hosts"
                    variable = getVariableString()
                    sh "ansible-playbook -i inventory -e password=${password} -e user=${user} ${variable} main.yaml"
                    
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

@NonCPS
def getVariableString(){
    command=""
    ["SERVERNAME=100", "SERVERVALUE=200"].each { item ->
        command += "-e ${item}"
    }
}