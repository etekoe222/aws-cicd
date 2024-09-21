pipeline{
    agent any

    environment {
        BRANCH_NAME = 'main'
        GIT_URL = 'https://github.com/etekoe222/aws-cicd.git'
    }

stages {
    stage('git checkout'){
        steps{
            git branch: "${branch_NAME}" , "${GIT_URL}"
        }
    }
    stage( 'docker build'){
        steps{
            sh 'docker build -t awscicd .'
            sh ' docker images'
        }
    }
    

}


}