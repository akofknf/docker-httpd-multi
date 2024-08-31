pipeline {

	agent {
		label {
			label "docker-vm"
			customWorkspace "/mnt/docker-pipeline-1/"
		}
	
	}
	stages {

		stage ("QA1") {
			steps {

				sh "docker run -itdp 8081:80 --name server-2 httpd"
				sh "sudo echo 'This is QA1 page from docker' > /mnt/docker-pipeline-1/index.html"
				sh "docker cp /mnt/docker-pipeline-1/index.html server-1:/usr/local/apache2/htdocs"
			}

		}


	}



}
