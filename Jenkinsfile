pipeline{
    agent any
    environment{
        IMAGETAG = "${env.GIT_COMMIT}"
    }
    stages{
        stage('docker login'){
            steps{
                sh "docker login -u botadmin -p Gangadhar@99 docker.io"

                echo "login success"
            }
        }
        stage('docker image build'){
            steps{
                sh "docker build -t botadmin/project1:${IMAGETAG}"
                echo "Image build is successful"
                sh "docker image ls"
            }
        }
        stage('docker image push'){
            steps{
                sh "docker push botadmin/project1:${IMAGETAG}"
            }
        }
            
        }
}
