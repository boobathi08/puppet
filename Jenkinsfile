pipeline {
    agent any
        stage("Docker build") {
     steps {
            sh "wget https://download.sonatype.com/nexus/oss/nexus-2.14.8-01-bundle.tar.gz"
            sh "docker build -t boobathi08/nexus -f /var/lib/jenkins/workspace/docker-test/Dockerfile"
             }
           }
     stage("Docker push") {
     steps {
    sh "docker login -u username -p password"
    sh "docker push boobathi08/nexus"
     }
}
      stage("Deploy to staging") {
        steps {
           sh "docker run -d --rm -p 8081:8081 --name boobathi08/nexus "
     }
}
}
