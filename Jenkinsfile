pipeline {
  agent any
  tools { nodejs 'Node' }
  parameters {
    string(name: 'executor', defaultValue: 'user', description: 'Nom de la persona que executa la pipeline')
    string(name: 'motiu', defaultValue: 'motiu', description: 'Motiu pel qual estem executant la pipeline')
    string(name: 'chatID', defaultValue: 'num_chat', description: 'ChatID de telegram per a notificar els resultats')
  }
  stages {
    stage('Petició de dades') {
      steps {
        sh "node index.js '${params.executor}'"
        sh "node index.js '${params.motiu}'"
        sh "node index.js '${params.chatID}'"
      }
    }
    stage('Linter') {
      echo "Linting"
    }
    stage('Test') {
      echo "Test"
    }
    stage('Build') {
      echo "Build"
    }
    stage('Update_Readme') {
      echo "Update Readme"
    }
    stage('Push_Changes') {
      echo "Push changes"
    }
    stage('Deploy to Vercel') {
      echo "Deploy to Vercel"
    }
    stage('Notificació') {
      echo "Notificació"
    }
  }
}