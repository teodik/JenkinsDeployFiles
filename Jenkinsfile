pipeline{
    agent any
    stages{
        stage('Deploy file'){
            steps{
                bat("COPY /a C:\\XebiaLabs\\temp\\script_output_20200218081914.log C:\\xebiaLabs\\stagin") 
                //sh "sh /XebiaLabs/temp/script_output_20200218081914.log teodik:teodik-VirtualBox:/home/teodik"
            }
        }
    }
}