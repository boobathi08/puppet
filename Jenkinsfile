pipeline {
    agent any
        stage("Docker build") {
     steps {
            sh "wget https://download.sonatype.com/nexus/oss/nexus-2.14.8-01-bundle.tar.gz"
            sh "docker build -t boobathi08/nexus -f /var/lib/jenkins/workspace/docker-test/Dockerfile"
             }
}
}
