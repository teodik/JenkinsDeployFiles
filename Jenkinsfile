pipeline{
    agent any
    stages{
        stage('Deploy file'){
            steps{
                cleanWs()
                bat('mkdir bitbucket')
                bat('mkdir github')
                dir('bitbucket'){
                    script{
                        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github-account', url: 'https://teodik1979@bitbucket.org/teodik1979/aggregate.git']]])
                    }
                }
                dir('github'){
                    script{
                        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github-account', url: 'https://github.com/teodik/aggregate.git']]])
                    }
                }
                bat('copy bitbubket/aggregate/README.md github/aggregate/README.md')
                dir('github/aggregate'){
                    bat('git push')
                }
            }
        }
    }
}
