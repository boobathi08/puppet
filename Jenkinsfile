pipeline {
    agent any
        stage("Docker build") {
     steps {
            sh "docker build -t boobathi08/nexus ."
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
