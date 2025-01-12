pipeline {
  agent any
  tools { nodejs 'Node' }
  parameters {
    string(name: 'executor', defaultValue: 'user', description: 'Nombre de la persona que ejecuta la pipeline')
    string(name: 'motiu', defaultValue: 'motiu', description: 'Motivo por el que se ejecuta la pipeline')
    string(name: 'chatID', defaultValue: 'num_chat', description: 'Chat ID de Telegram')
  }
  stages {
    stage('Execution') {
      steps {
        sh "node index.js '${params.executor}'"
        sh "node index.js '${params.motiu}'"
        sh "node index.js '${params.chatID}'"
      }
    }
  }
}