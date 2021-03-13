pipeline {
	
agent {
        docker { image 'microsoft/aspnetcore-build' }
    }
{ 
node {
    stage('Checkout git repo') {
      git branch: 'main', url: 'https://github.com/DenisKotolenko/LearnJenkins.git'
      sleep(60)
    }
	
    stage ('Build') {
	sh(script: 'dotnet --version', returnStdout: true);
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
