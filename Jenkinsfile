pipeline {
  agent any
  tools { nodejs 'Node'}
  parameters {
    string(name: 'persona_a_saludar', defaultValue: 'user', description: 'Nombre de la persona')
  }
  stages {
    stage('Execution') {
      steps {
        sh "node index.js '${params.persona_a_saludar}'"
      }
    }
  }
}