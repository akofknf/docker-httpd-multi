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

				sh "docker run -itdp 8080:80 --name server-1 httpd"
				sh "echo 'This is master page from docker' > /home/ec2-user/index.html"
				sh "docker cp /home/ec2-user/index.html server-1:/usr/local/apache2/htdocs/"
			}

		}


	}



}
