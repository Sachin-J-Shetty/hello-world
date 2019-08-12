node {

    def app

    stage('Clone repository') {
         checkout scm
         echo "Cloning the Repository to our Workspace"
    }

    stage('Build image') {
        app = docker.build("sachinjshetty/hello-world")
	echo "This builds the actual image"
    }

    stage('Push image') {
        /* 			
       You would need to first register with DockerHub before you can push images to your account
	*/

        docker.withRegistry('https://registry.hub.docker.com', 'docker-hub') {

            app.push("${env.BUILD_NUMBER}")

            app.push("latest")

            } 

                echo "Trying to Push Docker Build to DockerHub"

    }

}
