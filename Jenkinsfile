pipeline {
    agent any

    triggers {
        cron('*/3 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Checking Python program...'

                bat '"C:/Users/HP/AppData/Local/Programs/Python/Python314/python.exe" -m py_compile palindrome.py'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Python program...'

                bat 'echo madam | "C:/Users/HP/AppData/Local/Programs/Python/Python314/python.exe" palindrome.py'
            }
        }
    }
}
