pipeline{
    agent any
    stages{
        stage('always'){
            steps{
                echo "this is main steps always executable"
            }
        }
        stage('main steps'){
            when {branch 'main'}
            steps{
                echo "this is running from main branch"
            }
        }
        stage('fix-2 steps'){
            when {branch 'fix-2'}
            steps{
                echo "this is running from main branch"
            }
        }
        stage('fix-1 steps'){
            when {branch 'fix-1'}
            steps{
                echo "this is running from main branch"
            }
        }
    }
    post{
        always{
            echo "job finished"
        }
    }
}
