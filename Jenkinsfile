node {

	stage(' Clone PetClinic Source Code') {
	def git_branch = "main"
	def git_url = "https://github.com/madhavakondapalli402/spring-petclinic.git"
	git branch: "${git_branch}", url: "${git_url}"
	}
	
	stage('Build Package ') {
        jdk = tool name: 'JAVA_HOME', type: 'jdk'
        env.JAVA_HOME = "$jdk"
        def mvnHome = tool name: 'MAVEN_HOME', type: 'maven'
        sh "${mvnHome}/bin/mvn clean"
        sh "/opt/apache-maven-3.9.1/bin/mvn package"
	}
}
