pipeline {
  agent any
  tools {
    maven "Maven"
  }
  stages {
      stage("build") {
          steps {
            echo 'build ...'
           snDevOpsStep()
		  snDevOpsArtifact(artifactsPayload:"""{"artifacts": [{"name": "devops_pipeline_demo.jar","version": "1.2","semanticVersion": "1.2.0","repositoryName": "devops_pipeline_demo"}],"stageName": "build"}""")
   		sleep 5
	//snDevOpsChange()
          }
      }
      stage("test") {
           steps {
             echo 'test ..'
              snDevOpsStep()
  		sleep 5
           }
       }
      stage("deploy") {
          steps {
            echo 'Deploying..'
       snDevOpsStep()
		  
		sleep 5
		  snDevOpsChange()
          }
      }
  }
}
