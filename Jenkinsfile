pipeline {
    agent any

    stages {
        stage('Setup Python Environment') {
            steps {
                bat """
                "C:/Users/srela/AppData/Local/Programs/Python/Python311/python.exe" --version
                "C:/Users/srela/AppData/Local/Programs/Python/Python311/python.exe" -m venv venv
                call venv\\Scripts\\activate && python -m pip install --upgrade pip
                call venv\\Scripts\\activate && pip install -r "requirements (1).txt"
                """
            }
        }

        stage('Run Tests') {
            steps {
                bat """
                call venv\\Scripts\\activate && pytest
                """
            }
        }
    }
}