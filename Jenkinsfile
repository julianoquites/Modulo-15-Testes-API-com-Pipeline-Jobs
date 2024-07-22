pipeline {
    agent any
    stages {
        stage('Clonar repositório') {
            steps {
                git branch: 'main', url: 'https://github.com/julianoquites/Modulo-15-Testes-API-com-Pipeline-Jobs.git'
            }
        }
        stage('Instalar dependências') {
            steps {
                sh 'npm install'
            }
        }
        stage('Executar Testes') {
            steps {
                sh 'NO_COLOR=1 npm run cy:run'
            }
        }
    }
}