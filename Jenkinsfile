pipeline{
    agent any 
    stages{
        stage('Build'){
            steps{
                echo  "Builind... release ${env.BRANCH_NAME}"
            }
        }
        stage('Test'){
            steps{
                echo "Testing... release ${env.CHANGE_ID}"
            }
        }
    }
}