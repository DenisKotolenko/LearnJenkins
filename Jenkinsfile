node {
    stage('Checkout git repo') {
      git branch: 'main', url: 'https://github.com/DenisKotolenko/LearnJenkins.git'
    }
	  stage 'Build'
		  bat 'nuget restore LearnJenkinsMvc.csproj'
		  bat "\"${tool 'MSBuild'}\" LearnJenkinsMvc.csproj /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"


    // stage('deploy') {
    //     azureWebAppPublish azureCredentialsId: params.azure_cred_id,
    //         resourceGroup: params.res_group, appName: params.customersapiapp, sourceDirectory: "src/CustomersAPI/bin/Release/netcoreapp2.1/publish/"
    //     azureWebAppPublish azureCredentialsId: params.azure_cred_id,
    //         resourceGroup: params.res_group, appName: params.customersmvcapp, sourceDirectory: "src/CustomersMVC/bin/Release/netcoreapp2.1/publish/"
    // }
}