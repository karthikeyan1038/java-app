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
				sh 'mv /home/zippyops/jenkins/workspace/chef-project/java-sample-app/target/java-sample-app-1.0.0.war /root/chef-repo/cookbooks/tomcat8/files'
	}
}
	}
}
