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
            sh 'curl -fsSL https://raw.githubusercontent.com/ZupIT/horusec/main/deployments/scripts/install.sh | bash -s latest'
            sh 'horusec start -p="./" -e="true"'
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
