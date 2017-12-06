pipeline {
    agent none
    stages {
	stage('Parallel Stage') {
        when {
                branch 'master'
            }
	    parallel {
                stage('Build-slave1') {
	        agent { node { label 'slave-1' } }
                    steps {
                        echo 'Building..'
		        sh 'mkdir /home/ec2-user/jenkin/slave-1/subdir1'
                    }
                }
	        stage('Build-slave2') {
	        agent { node { label 'slave-2' } }
                    steps {
                        echo 'Building..'
                        sh 'mkdir /home/ec2-user/jenkin/slave-2/subdir1'
                    }
                }
            }
        }
    }
    post {
        success {
            echo 'I will always say Hello again!'
        }
    }
}
