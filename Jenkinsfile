pipeline {
  agent any
  stages {
    stage('Ejecutar build') {
      steps {
        build 'Proyecto Maven2'
      }
    }

    stage('crear carpeta') {
      steps {
        bat 'cd C:\\ProgramData\\Jenkins\\.jenkins\\workspace'
        bat 'IF exist empaquetado/nul ( echo empaquetado ya existe ) ELSE ( mkdir empaquetado && echo empaquetado creada)'
      }
    }

    stage('mover archivo war') {
      steps {
        bat 'MOVE "C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\Proyecto Maven2\\Jenkins2\\target\\Jenkins2-1.0-SNAPSHOT.war" "C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\empaquetado"'
      }
    }

  }
}