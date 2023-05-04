node {

	stage(' Clone PetClinic Source Code') {
	git 'https://github.com/madhavakondapalli402/spring-petclinic.git'
	}
	
	stage('Build Package ') {
	def MNHOME = tool name: 'MAVEN_HOME', type: 'maven'
	sh "${MNHOME}/bin/mvn package"
	}
}
