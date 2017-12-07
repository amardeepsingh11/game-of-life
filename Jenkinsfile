pipeline {
    agent { node { label 'slave-1' } }
    stages {
        stage('Build-slave1') {
	   steps {
                echo 'Building..'
		sh 'mvn --version'
            }
        }
    }
    post {
        success {
            echo 'I will always say Hello again!'
        }
    }
}
