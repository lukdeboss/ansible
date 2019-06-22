
// to komewntarz
pipeline {
    agent any

    stages {
        stage('instalacja ansible') {
            steps {
                echo 'instalacja ansible'
                sh 'setenforce Permissive'     //wylaczenie selinux
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


