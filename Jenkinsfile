node {
    stage('Checkout git repo') {
      git branch: 'main', url: 'https://github.com/DenisKotolenko/LearnJenkins.git'
    }
    stage('build and publish') {
        sh(script: "dotnet publish .\LearnJenkins.csproj -c Release ", returnStdout: true)
    }

    // stage('deploy') {
    //     azureWebAppPublish azureCredentialsId: params.azure_cred_id,
    //         resourceGroup: params.res_group, appName: params.customersapiapp, sourceDirectory: "src/CustomersAPI/bin/Release/netcoreapp2.1/publish/"
    //     azureWebAppPublish azureCredentialsId: params.azure_cred_id,
    //         resourceGroup: params.res_group, appName: params.customersmvcapp, sourceDirectory: "src/CustomersMVC/bin/Release/netcoreapp2.1/publish/"
    // }
}