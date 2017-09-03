def username = 'Jenkins'

pipeline {
    agent any
    
    stages {
        stage('Get source code') {
            steps {
                git url: 'git@gitlab.kkinternal.com:garycheng/Login_API.git'
            }
        }
        
        stage('Test') {
            steps {
                sh 'pytest -v test_login_api.py'
            }
        }
    }
    
    //post {
    //    always {
    //       sh 'pytest -v test_login_api.py'
    //    }
    //    failure {
    //        mail to: 'garycheng@kkbox.com', subject: 'job fail'
    //    }
    //}
}
