pipeline{
    agent none 
    stages{
        stage('Back-end'){
            agent{
                docker { image 'maven:3-alpine' }
            }
            steps{
                sh 'mvn --version'
                sh 'touch arquivo.txt'
                sh 'echo "rodrigo ribeiro" >> arquivo.txt'
                stash includes:'arquivo.txt' name: 'arquivo'
            }
        }
        stage('Front-end'){
            agent{
                docker { image 'node:7-alpine' }
            }
            steps{
                sh 'node --version'
                unstash 'arquivo'
                sh "cat arquivo.txt"
            }
        }
    }
}