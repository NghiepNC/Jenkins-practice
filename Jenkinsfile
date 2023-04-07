pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
		}
		stage('Build docker'){
			steps{
				withDockerRegistry(credentialsId: '40ce2dd8-5adf-40b7-843c-c0b64f8f6efb', url: 'https://index.docker.io/v1/') {
    				sh 'docker build -t karimcn/Jenskin-practice:v10'
					sh 'docker push -t karimcn/Jenskin-practice:v10'
				}

			}
		}
        
    }
}

