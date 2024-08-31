pipeline {

	agent {
		label {
			label "docker-vm"
			customWorkspace "/mnt/docker-pipeline-3/"
		}
	
	}
	stages {

		stage ("QA3") {
			steps {

				sh "docker run -itdp 8083:80 --name server-3 httpd"
				sh "sudo echo 'This is QA3 page from docker' > /mnt/docker-pipeline-3/index.html"
				sh "docker cp /mnt/docker-pipeline-3/index.html server-3:/usr/local/apache2/htdocs"
			}

		}


	}



}
