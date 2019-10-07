pipeline {
    agent any

    options {
        buildDiscarder(logRotator(daysToKeepStr: '7'))
    }

    triggers {
        cron('* * * * *')
    }

    stages {
        stage('Build') {
            when { branch 'master' }
            steps {                
                    sh 'python -m virtualenv venv'
                    sh 'source ./venv/bin/activate'
                    sh '`which ping` -c 10 www.google.com'
                }
            }
        }
}
