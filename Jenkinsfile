node {

	stage(' Clone PetClinic Source Code') {
	def git_branch = "main"
	def git_url = "https://github.com/madhavakondapalli402/spring-petclinic.git"
	git branch: "${git_branch}", url: "${git_url}"
	}
	
	stage('Build Package ') {
        sh "mvn clean"
        sh "mvn package"
	}
}
