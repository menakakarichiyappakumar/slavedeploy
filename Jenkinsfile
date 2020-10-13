pipeline{
    agent any
    stages{
        stage("Deployment"){
            //using the docker template
            agent {
                label 'slave'
            }
            //using the slave node ubuntu
            steps{
                sshagent(['ubuntu']){
                   sh 'ssh -o StrictHostKeyChecking=no ubuntu@18.221.32.39 sudo docker run -d -p 80:8080 menakakarichiyappakumar/springboot'
                }
            }
        }
        
    }
}
