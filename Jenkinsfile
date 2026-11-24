pipeline {

    agent {
        label "AGENT-1"
    }

    environment {
        COURSE = "Jenkins"
    }

    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'vidya')
    }
    stages {
        stage('build'){
            steps {
                echo "this is build..."
                env 
                echo "Hello, ${params.PERSON}"
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
                        cat script.txt
                    """
                }
            }
        }
    }

    post {
        success {
            echo "Hello Success"
            deleteDir()
        }
        failure {
            echo "Hello Failure"
        }
    }

}