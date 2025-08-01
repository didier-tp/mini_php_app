pipeline {
    //agent any
    agent {
        docker {  image 'php:8.3-apache' 
				}
     }
	environment{
		docker_image_name='didierdefrance69/mini_php_app:1'
	}
    stages {
	    //stage('from_git') {
        //    steps {
        //          git url : 'https://github.com/didier-tp/mini_php_app' , branch : 'main'
        //    }
        //}
        
		stage('test') {
            steps {
				echo 'test en php ....'
	
            }
        }
		stage('build_docker_image') {
			steps {
            //with Pipeline docker plugin:
			  script{
				    echo "docker_image_name=" + docker_image_name
					dockerImage = docker.build(docker_image_name)
				  }
			   }
        }
    }
}
