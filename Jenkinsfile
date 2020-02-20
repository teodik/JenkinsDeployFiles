pipeline{
    agent any
    stages{
        stage('Deploy file'){
            steps{
                bat "COPY C:\XebiaLabs\temp\script_output_20200218081914.txt teodik:teodik-VirtualBox:/home/teodik" 
                //sh "sh /XebiaLabs/temp/script_output_20200218081914.txt teodik:teodik-VirtualBox:/home/teodik"
            }
        }
    }
}