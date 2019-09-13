pipeline {
  agent any
  tools {
    maven "Maven"
  }
  stages {
      stage("Build") {
          steps {
            echo 'build ..........'
              snDevOpsStep '0d35bc32db77f300e10d77bcbf9619f0'
              sh 'mvn clean install'
          }
      }
      stage("Test") {
           steps {
             echo 'test .......'
                snDevOpsStep '8935bc32db77f300e10d77bcbf9619f0'
                snDevOpsChange()
                sh 'mvn test -Dpublish'
                junit '**/target/surefire-reports/*.xml'
           }
       }
      stage("Deploy") {
          steps {
            echo 'Deploying....... '
            snDevOpsStep '8d35bc32db77f300e10d77bcbf9619f0'
            snDevOpsChange()
          }
      }
  }
}
