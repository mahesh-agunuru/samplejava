pipeline {
  agent any
  tools {
    maven "Maven"
  }
  stages {
      stage("Build") {
          steps {
            echo 'build ......'
              snDevOpsStep()
              sh 'mvn clean install'
          }
      }
      stage("Test") {
           steps {
             echo 'test .....'
                snDevOpsStep()
                sh 'mvn test -Dpublish'
                junit '**/target/surefire-reports/*.xml'
           }
       }
      stage("Deploy") {
          steps {
            echo 'Deploying....'
            snDevOpsStep()
            snDevOpsChange()
            sh 'mvn test -Dpublish'
            junit '**/target/surefire-reports/*.xml'
          }
      }
  }
}
