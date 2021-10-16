pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                    git branch: 'main', url: 'git@github.com:DKosimov/devops21-jenkins-public.git'
                }
            }

        stage ('Test') {
            steps {
                script{
                    sh "chmod +x -R ${env.WORKSPACE}/../${env.JOB_NAME}/test.sh"
                }
            }
        }
    }
}
