pipeline{

    agent any

    stages{
        stage('Checkout the code'){
            steps{
                git branch: 'main', url: 'https://github.com/skmdab/create_jenkins.git'
            }
        }

        stage('Creating server'){
            steps{
                sh "sh aws_create.sh"
            }
        }

        stage('Installing jenkins package into server'){
            steps{
                withCredentials([file(credentialsId: 'pemfile', variable: 'PEMFILE')]) {
		   sh 'ansible-playbook installjenkins.yaml --private-key="$PEMFILE"'
		}
            }
        }
    }
}
