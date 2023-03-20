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
          packagePath: "C:\ProgramData\Jenkins\.jenkins\workspace\Uipath_Pipeline_main\Output\14\CICD_process.1.0.14.nupkg",
          orchestratorAddress: "https://cloud.uipath.com/eidikosggfpo",
          orchestratorTenant: "DefaultTenant",
          folderName: "Shared",
          environments: "environment",
          credentials: [$class: 'UserPassAuthenticationEntry', credentialsId: “	Api_key”],
          traceLoggingLevel: 'None'
        )
      }
    }
  }
	      
}
