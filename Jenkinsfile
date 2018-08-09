node {
 	// Clean workspace before doing anything
    deleteDir()

    try {
	stage("Docker build") {
     		steps {
	          	sh "wget https://download.sonatype.com/nexus/oss/nexus-2.14.8-01-bundle.tar.gz ."
          		sh "docker build -t boobathi08/nexus ."
			
      	}
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
} 
}
