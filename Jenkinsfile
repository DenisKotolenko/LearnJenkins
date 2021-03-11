podTemplate(containers: [
    containerTemplate(name: 'dotnet-sdk', image: 'microsoft/dotnet:2.2-sdk', ttyEnabled: true, command: 'cat'),
]) 
{ 
node {
    stage('Checkout git repo') {
      git branch: 'main', url: 'https://github.com/DenisKotolenko/LearnJenkins.git'
      sleep(60)
    }
	
    stage ('Build') {
	sh(script: 'dotnet build LearnJenkins.csproj', returnStdout: true);
    }
	
    stage ('Create docker image') {
	echo 'TODO'
	echo 'created image'
    }
	
    stage ('Deploy HELM to Kubernetes') {
	echo 'TODO'
	echo 'published to GKE'
    }
}
	
}
