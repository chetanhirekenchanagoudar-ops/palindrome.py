pipeline {
    agent any

    triggers {
        cron('*/3 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Checking Python program...'
                bat 'py -m py_compile palindrome.py'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Python program...'
                bat 'echo madam | py palindrome.py'
            }
        }
    }
}
