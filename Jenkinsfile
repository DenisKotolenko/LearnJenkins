pipeline {
	
agent {
        docker { image 'microsoft/aspnetcore-build' }
    }
stages {
    stage('Checkout git repo') {
      git branch: 'main', url: 'https://github.com/DenisKotolenko/LearnJenkins.git'
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
