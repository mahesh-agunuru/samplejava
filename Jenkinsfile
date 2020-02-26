pipeline {
  agent any
  tools {
    maven "Maven"
  }
  stages {
      stage("build") {
          steps {
            echo 'build ....'
              snDevOpsStep()
              sleep 5
          }
      }
      stage("test") {
           steps {
             echo 'test .....'
                snDevOpsStep()
                sleep 5
           }
       }
      stage("deploy") {
          steps {
            echo 'Deploying..'
            snDevOpsStep()
            sleep 5
            //snDevOpsChange()
            //sh 'mvn test -Dpublish'
            //junit '**/target/surefire-reports/*.xml'
          }
      }
  }
}
