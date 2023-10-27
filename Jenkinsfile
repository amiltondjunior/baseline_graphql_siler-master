pipeline {
    agent any
    stages {
        stage('Preparação') {
            steps {
                // Etapas de preparação, como clonar o repositório, instalar dependências, etc.
                sh 'echo "Executando etapa de preparação"'
            }
        }
        stage('Construção') {
            steps {
                // Etapas para construir seu aplicativo ou projeto.
                sh 'echo "Executando etapa de construção"'
            }
        }
        stage('Testes') {
            steps {
                // Etapas para executar testes automatizados.
                sh 'echo "Executando etapa de testes"'
            }
        }

        stage('Security') {
          steps {
            sh 'ulimit -n 4096'
            sh 'horusec start -D -p . -w -e="true" -i **/*.crt,**/pt-BR.json,**/*.pem,**/*helpers*,**/*Test*,**/README.md,**/*.key,**/*spec.tsx,**/*keycloak.ts'
        }
    }

        stage('Implantação') {
            steps {
                // Etapas para implantar seu aplicativo.
                sh 'echo "Executando etapa de implantação"'
            }
        }
    }
}
