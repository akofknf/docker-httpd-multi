pipeline {

	agent {
		label {
			label "docker-vm"
			customWorkspace "/mnt/docker-pipeline-2/"
		}
	
	}
	stages {

		stage ("QA2") {
			steps {

				sh "docker run -itdp 8082:80 --name server-2 httpd"
				sh "sudo echo 'This is QA2 page from docker' > /mnt/docker-pipeline-2/index.html"
				sh "docker cp /mnt/docker-pipeline-2/index.html server-2:/usr/local/apache2/htdocs"
			}

		}


	}



}
