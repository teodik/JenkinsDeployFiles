pipeline{
    agent any
    environment{
        source = ''
        destination = ''
    }
    stages{
        stage("interactive input"){
            steps{
                script{
                    //def source
                    //def destination
                    def userInput = input(
                        id: 'userInput', message: 'Enter source & destination path:', parameters:[
                            string(defaultValue: 'none', description: 'Path for source file', name: 'src'),
                            string(defaultValue: 'none', description: 'Path for destination file', name: 'dest')
                        ]
                    )
                    source = userInput.src
                    destination = userInput.dest
                    echo("source: ${source}")
                    echo("destination: ${destination}")
                }
            }
        }
        stage('Deploy file'){
            steps{
                bat("COPY /a ${source} ${destination}")
                //bat("pscp -pw 27may1979 C:\\XebiaLabs\\temp\\script_output_20200218081914.log teodik@10.0.2.15:/home/teodik") //pscp is downloaded https://comtechies.com/copy-files-between-windows-and-linux.html
                //bat("COPY /a C:\\XebiaLabs\\temp\\script_output_20200218081914.log C:\\xebiaLabs\\stagin") 
                //sh "scp /XebiaLabs/temp/script_output_20200218081914.log teodik@teodik-VirtualBox:/home/teodik"
            }
        }
    }
}