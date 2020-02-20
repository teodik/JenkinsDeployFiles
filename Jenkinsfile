pipeline{
    agent any
    stages{
        stage('Deploy file'){
            steps{
                bat "COPY /XebiaLabs/temp/script_output_20200218081914.txt /xebiaLabs/stagin" 
                //sh "sh /XebiaLabs/temp/script_output_20200218081914.txt teodik:teodik-VirtualBox:/home/teodik"
            }
        }
    }
}