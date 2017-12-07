pipeline {
    agent { node { label 'slave-1' } }
    stages {
        stage('Build-slave1') {
	   steps {
                echo 'Building..'
		sh 'mvn --version'
		sh 'mvn clean install -B -U -Dsurefire.useFile=false'
            }
        }
        stage('Build-slave1') {
           steps {
                echo 'installing on i'
            }
        }
    }
    post {
        success {
            echo 'I will always say Hello again!'
        }
    }
}
