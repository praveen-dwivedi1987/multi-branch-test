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
        stage('take input'){
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
            steps{
                echo "this is hello to $PERSON"
            }
        }
    }
    post{
        always{
            echo "job finished"
        }
    }
}
