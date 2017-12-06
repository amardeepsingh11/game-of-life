pipeline {
    agent { node { label 'slave-1' } }
    stages {
	agent { node { label 'slave-1' } }
        stage('Build-slave1') {
            steps {
                echo 'Building..'
		sh 'mkdir /home/ec2-user/jenkin/slave-1/subdir'
            }
        }
	stage('Build-slave2') {
	agent { node { label 'slave-2' } }
            steps {
                echo 'Building..'
                sh 'mkdir /home/ec2-user/jenkin/slave-1/subdir'
            }
        }
    }
    post {
        success {
            echo 'I will always say Hello again!'
        }
    }

}
