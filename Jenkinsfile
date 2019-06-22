
// to komewntarz
pipeline {
    agent { label: 'glowne' }
    environment {
       PATH="/bin:/sbin:/usr/bin"
    }
    stages {
        stage('check ansible') {
            steps {
            ansiblePlaybook(inventory: 'inventory', playbook: 'playbook.yaml')
            sh 'uname -a'
            sh 'ls -al /bin'
            sh 'ls -al /usr/bin'        
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


