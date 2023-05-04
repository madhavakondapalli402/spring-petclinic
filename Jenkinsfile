node {

	stage(' Clone PetClinic Source Code') {
	def git_branch = "main"
	def git_url = "https://github.com/madhavakondapalli402/spring-petclinic.git"
	git branch: "${git_branch}", url: "${git_url}"
	}
	
	stage('Build Package ') {
        def mvnHome = tool name: 'MAVEN_HOME', type: 'maven'
        sh "${mvnHome}/bin/mvn clean"
        sh "${mvnHome}/bin/mvn package"
	}
}
