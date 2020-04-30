pipeline{
    agent any
    stages{
        stage('Deploy file'){
            steps{
                bat('mkdir bitbucket')
                bat('mkdir github')
                dir('bitbucket'){
                    bat('git clone https://teodik1979@bitbucket.org/teodik1979/aggregate.git')
                }
                dir('github'){
                    bat('git clone https://github.com/teodik/aggregate.git')
                }
                bat('copy bitbubket/aggregate/README.md github/aggregate/README.md')
                dir('github/aggregate'){
                    bat('git push')
                }
            }
        }
    }
}
