pipeline {
   agent any
   stages {
       stage("build") {
           steps {
               snDevOpsStep '631dc9cd135b7300bcc3b2776144b038'
               echo "Building"
               sleep 5
           }
       }
       stage("test") {
           steps {
               snDevOpsStep '6b1dc9cd135b7300bcc3b2776144b037'
               echo "Testing"
               sleep 3
           }
       }
       stage("deploy") {
           steps {
               snDevOpsStep 'e31dc9cd135b7300bcc3b2776144b038'
               echo "Deploying"
               sleep 7
           }
       }
       stage("prod") {
           steps {
               snDevOpsStep '671dc9cd135b7300bcc3b2776144b038'
               echo "production"
               sleep 7
           }
       }
   }
}
