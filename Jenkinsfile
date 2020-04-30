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
                    bat("git filter-branch --index-filter 'rm .gitmodules' HEAD")
                    bat('dir')
                }
                dir('github'){
                    script{
                        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github-account', url: 'https://github.com/teodik/aggregate.git']]])
                    }
                    bat('dir')
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
