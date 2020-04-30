pipeline{
    agent any
    stages{
        stage('Deploy file'){
            steps{
                bat('mkdir bitbucket')
                bat('mkdir github')
                bat('dir')
                dir('bitbucket'){
                    script{
                        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github-account', url: 'https://teodik1979@bitbucket.org/teodik1979/aggregate.git']]])
                    }
                    bat('dir')
                }
                dir('github'){
                    script{
                        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github-account', url: 'https://github.com/teodik/aggregate.git']]])
                    }
                    bat('dir')
                }
                bat('copy bitbucket/aggregate/README.md github/aggregate/README.md')
                dir('github/aggregate'){
                    bat('git push')
                }
            }
        }
    }
    post{
        always{
            cleanWs()
        }
    }
}
