pipeline {

    agent {
        label "AGENT-1"
    }
    stages {
        stage('build'){
            steps {
                echo "this is build..."
            }
        }
        stage('test'){
            steps {
                echo "this is testing..."
            }
        }
        stage('deploy'){
            steps {
                echo "this is deploying...."
            }
        }
        stage('scripted'){
            steps {
                script {
                    sh """
                        echo "Hello this is scripted" > script.txt
                        car script.txt
                    """
                }
            }
        }
    }

}