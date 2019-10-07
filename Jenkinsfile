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
                    sh '`which python3.6` -m venv ./venv'
                    sh 'source ./venv/bin/activate && `which ping` -c 10 www.google.com'
                }
            }
        }
}
