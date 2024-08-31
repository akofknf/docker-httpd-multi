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

				sh "docker run -itdp 8081:80 --name server-2 httpd"
				sh "echo 'This is QA1 page from docker' > /home/ec2-user/index.html"
				sh "docker cp /home/ec2-user/index.html server-1:/usr/local/apache2/htdocs/"
			}

		}


	}



}
