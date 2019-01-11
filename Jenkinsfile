pipeline {
	agent {label 'krishna'}
	stages {
        stage ('checkout') {
            steps {
		checkout scm
            }
        }
        stage ('Build') {
            steps {
                sh '${m2_home}/bin/mvn -f java-sample-app/pom.xml clean install' 
            }
        }
		stage ('move') {
			steps {
				sh 'mv /root/home/zippyops/jenkins/workspace/TestProject/java-sample-app/target/java-sample-app-1.0.0.war /root/etc/puppetlabs/code/environments/production/modules/arjuna/files'
	}
}
	}
}
