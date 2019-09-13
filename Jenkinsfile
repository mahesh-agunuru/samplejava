pipeline {
  agent any
  tools {
    maven "Maven"
  }
  stages {
      stage("Build") {
          steps {
            echo 'build ........'
              snDevOpsStep '044eacbadb37f300e10d77bcbf9619e7'
              sh 'mvn clean install'
          }
      }
      stage("Test") {
           steps {
             echo 'test .....'
                snDevOpsStep '804eacbadb37f300e10d77bcbf9619e7'
                //snDevOpsChange()
                sh 'mvn test -Dpublish'
                junit '**/target/surefire-reports/*.xml'
           }
       }
      stage("Deploy") {
          steps {
            echo 'Deploying...... '
            snDevOpsStep '884eacbadb37f300e10d77bcbf9619e6'
            sh 'mvn test -Dpublish'
            junit '**/target/surefire-reports/*.xml'
          }
      }
  }
}
