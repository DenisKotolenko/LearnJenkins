
  node (POD_LABEL) {
    stage('Checkout git repo') {
      git branch: 'main', url: 'https://github.com/DenisKotolenko/LearnJenkins.git'
    }
	  
stage('Dotnet build') {

        container('dotnetbuilder') {
          sh(script: 'dotnetBuild project: 'LearnJenkinsMvc.csproj', sdk: 'DotNetSdk'', returnStdout: true);
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
