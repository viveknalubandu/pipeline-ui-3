pipeline {
  agent any
  tools {
    maven "Maven"
  }
  stages {
      stage("build") {
          steps {
            echo 'build ...'
           
   		sleep 5
          }
      }
      stage("test") {
           steps {
             echo 'test ..'
              
  		sleep 5
           }
       }
      stage("deploy") {
          steps {
            echo 'Deploying..'
       
		sleep 5
          }
      }
  }
}
