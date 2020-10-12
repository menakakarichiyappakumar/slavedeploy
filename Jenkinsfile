pipeline{
    agent any
    stages{
        stage("Deployment"){
            agent {
                label 'slave'
            }
            steps{
                sshagent(['ubuntu']){
                   sh 'ssh -o StrictHostKeyChecking=no ubuntu@3.19.185.172 sudo docker run -d -p 80:8080 menakakarichiyappakumar/springboot'
                }
            }
        }
        
    }
}
