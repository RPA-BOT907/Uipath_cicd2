pipeline {
  agent any
  environment {
      MAJOR = '1'
      MINOR = '0'
  }
  stages {
    stage ('PostBuild') {
      steps {
        UiPathDeploy (
          packagePath:"path\C:\ProgramData\Jenkins\.jenkins\workspace\Uipath_Pipeline_main\Output\14\to\NuGetpackage",
          orchestratorAddress: "https://cloud.uipath.com/eidikosggfpo",
          orchestratorTenant: "DefaultTenant",
          folderName: "Shared",
          environments: "environment",
          credentials: [$class: 'UserPassAuthenticationEntry', credentialsId: “Api_key”],
          traceLoggingLevel: 'None'
        )
      }
    }
  }
	      
}
