pipeline {
  agent any
  tools {
    maven "Maven"
  }
  stages {
      stage("build") {
          steps {
            echo 'build ...'
           //snDevOpsStep()
//snDevOpsArtifact(artifactsPayload:"""{"artifacts": [{"name": "devops_pipeline_demo.jar","version": "1.8","semanticVersion": "1.8.0","repositoryName": "devops_pipeline_demo"}],"stageName": "build"}""")
   		sleep 5
	//snDevOpsChange()
          }
      }
      stage("test") {
           steps {
             echo 'test ..'
	sh 'mvn clean test -Dpublish'
                junit '**/target/surefire-reports/*.xml'
              //snDevOpsStep()
  		sleep 5
           }
       }
      stage("deploy") {
          steps {
            echo 'Deploying.'
       //snDevOpsStep()
	//snDevOpsPackage(name: "devops_pipeline_demo", artifactsPayload: """{"artifacts": [{"name": "devops_pipeline_demo.jar","version": "1.8","semanticVersion": "1.8.0","repositoryName": "devops_pipeline_demo"}]}""")            
		sleep 5
		snDevOpsChange()
          }
      }
  }
}
