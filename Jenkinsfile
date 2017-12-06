pipeline {
    agent { node { label 'slave-1' } }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		sh 'mkdir /home/ec2-user/jenkin/slave-1/subdir'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
        success {
            echo 'I will always say Hello again!'
        }
    }

}
