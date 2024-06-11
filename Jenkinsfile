pipeline {
    agent any

    stages{

        stage("Code Checkout"){
            steps{
                git url:"https://github.com/krishnabd88/flask-todo.git", 
                    branch:"main"
            }
        }
        stage("Code build: Docker-docker build"){
            steps{    
               
                sh "docker build -t krishnabd88/flask-todo:latest ."
            }
        
        }
    
        stage("Code Deploy: Docker-deploy"){
            steps{    
               
                sh "docker run -d -t -p 8000:8000 krishnabd88/flask-todo:latest"
            }
        
        }
    
    }

}
