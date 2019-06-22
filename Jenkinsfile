
// to komewntarz
pipeline {
    agent any
    environment {
       PATH="/bin:/sbin:/usr/bin"
    }
    stages {
        stage('check ansible') {
            steps {
            sh 'ansible --version'
            }
        }
        stage('instalacja ansible') {
            steps {
                echo 'instalacja ansible'
                sh 'ls -al'     //wylaczenie selinux
                sh 'ls -al /'
                sh "ls -al /bin/yum /sbin/yum"
                sh 'yum -y install ansible'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                echo "zakladam ze to jest tutaj"
                sh 'ls -al '
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}


