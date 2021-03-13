podTemplate(containers: [
  containerTemplate(name: 'dotnetbuilder', image: 'mcr.microsoft.com/dotnet/aspnet', command: 'cat', ttyEnabled: true),
  containerTemplate(name: 'kubectl', image: 'lachlanevenson/k8s-kubectl:v1.8.8', command: 'cat', ttyEnabled: true),
  containerTemplate(name: 'helm', image: 'lachlanevenson/k8s-helm:latest', command: 'cat', ttyEnabled: true)
]) {
  node (POD_LABEL) {
    stage('Checkout git repo') {
      git branch: 'main', url: 'https://github.com/DenisKotolenko/LearnJenkins.git'
    }
	  
stage('Dotnet build') {

        container('dotnetbuilder') {
          sh(script: 'dotnet --version', returnStdout: true);
        }
  
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
