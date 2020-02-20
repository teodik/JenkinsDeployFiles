pipeline{
    agent any
    stages{
        stage('Deploy file'){
            steps{
                bat("COPY /a /z C:\\XebiaLabs\\temp\\script_output_20200218081914.log teodik@10.0.2.15:/home/teodik")
                //bat("COPY /a C:\\XebiaLabs\\temp\\script_output_20200218081914.log C:\\xebiaLabs\\stagin") 
                //sh "scp /XebiaLabs/temp/script_output_20200218081914.log teodik@teodik-VirtualBox:/home/teodik"
            }
        }
    }
}