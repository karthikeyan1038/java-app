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
	#	stage('move') {
	#		steps {
	#		 sh 'mv /home/zippyops/jenkins/java-app/simple-java-app/target/*.war /etc/puppetlabs/code/environment/production/modules'
    #}
#}
	}
}
