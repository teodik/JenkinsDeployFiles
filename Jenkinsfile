pipeline{
    agent any
    stages{
        stage('Deploy file'){
            steps{
                bat("COPY /a C:\\XebiaLabs\\temp\\script_output_20200218081914.txt C:\\xebiaLabs\\stagin") 
                //sh "sh /XebiaLabs/temp/script_output_20200218081914.txt teodik:teodik-VirtualBox:/home/teodik"
            }
        }
    }
}