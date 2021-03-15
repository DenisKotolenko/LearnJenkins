def podLabel = "buildpod_" + "${env.JOB_NAME}.${env.BUILD_NUMBER}".replaceAll('[^A-Za-z0-9]', '_').reverse().take(54).reverse()

podTemplate(label: podLabel, containers: [
    containerTemplate(name: 'golang', image: 'golang:1.8.0', ttyEnabled: true, command: 'cat', privileged: true) 
]) {
  node(podLabel) {
    stage('Checkout git repo') {
      git branch: 'main', url: 'https://github.com/DenisKotolenko/LearnJenkins.git'
    }
	  
	stage('Build docker image')
	  stage('push docker image on repo')
	  stage('deploy docker image on kube')
	  
stage('Get a Golang project') {
            git url: 'https://github.com/hashicorp/terraform.git'
            container('golang') {
                stage('Build a Go project') {
                    sh """
                    mkdir -p /go/src/github.com/hashicorp
                    ln -s `pwd` /go/src/github.com/hashicorp/terraform
                    cd /go/src/github.com/hashicorp/terraform && make core-dev
                    """
                }
            }
        }
	

    stage ('Create docker image') {
	echo 'TODO'
	echo 'created image'
    }
	  stage('push docker image on repo') {
		  echo 'TODO'
	echo 'pushed image'
	  }
	
    stage ('Deploy HELM to Kubernetes') {
	echo 'TODO'
	echo 'published to GKE'
    }
}
	
}
