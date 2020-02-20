pipeline{
    agent any
    stages{
        stage('Deploy file'){
            steps{
                bat "scp /XebiaLabs/temp/script_output_20200218081914.txt teodik:teodik-VirtualBox:/home/teodik" 
            }
        }
    }
}