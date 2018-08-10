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
                      sh "sudo docker build -t boobathi08/nexus ."
                 }
            }
  stage("Package") {
       steps {
            sh "sudo docker run -d -p 8081:8081 boobathi08/nexus"
            sh "sudo rm -rf nexus-2.14.8-01-bundle.tar.gz"
       }
  }
  }
  }
