  pipeline {
       agent any
       stages {
            stage("Compile") {
                 steps {
                      sh "wget https://download.sonatype.com/nexus/oss/nexus-2.14.8-01-bundle.tar.gz"
                 }
            }
            stage("Unit test") {
                 steps {
                      sh "docker build -t boobathi08/nexus ."
                 }
            }
  stage("Package") {
       steps {
            sh "docker run -d -p 8081:8081 nexus"
       }
  }
  }
  }
