node {
    stage('Checkout git repo') {
      git branch: 'main', url: 'https://github.com/DenisKotolenko/LearnJenkins.git'
    }
	
    stage ('Build') {
	sh(script: 'dotnet build LearnJenkins.csproj', returnStdout: true);
    }
	
    stage ('Create docker image') {
	echo 'TODO'
	echo 'created image'
    }
	
    stage ('Publish docker image to GKE') {
	echo 'TODO'
	echo 'published to GKE'
    }
}
