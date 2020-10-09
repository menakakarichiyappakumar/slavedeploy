pipeline{
    agent any
    stages{
        stage("Deployment"){
            agent {
                label 'slave'
            }
            steps{
                sshagent(['ubuntu']){
                   sh 'ssh -o StrictHostKeyChecking=no ubuntu@18.220.126.39 sudo docker run -d -p 80:8080 menakakarichiyappakumar/springboot'
                }
            }
        }
        
    }
}
