pipeline {

	agent {
		label {
			label "docker-vm"
			customWorkspace "/mnt/docker-pipeline/"
		}
	
	}
	stages {

		stage ("master") {
			steps {

				sh "docker run -itdp 8080:80 --name server httpd"
				sh "sudo echo 'This is master page from docker' > /mnt/docker-pipeline/index.html"
				sh "docker cp /mnt/docker-pipeline/index.html server:/usr/local/apache2/htdocs"
			}

		}


	}



}
