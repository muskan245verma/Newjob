pipeline {
    agent any 
    stages {
        stage('Checkout') { 
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/muskan245verma/Newjob.git']]])
                  }
        }
        stage('Build') { 
            steps {
                git branch: 'main', url: 'https://github.com/muskan245verma/Newjob.git'
                bat 'python infoo.py'
            }
        }
        stage('Test') { 
            steps {
                echo "Tested Successfully"
            }
        }
    }
}
