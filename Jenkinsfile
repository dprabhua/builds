pipeline {
  agent any

  stages {

  stage('Git checkout ') {
  steps {
    parallel(
      Database: {
        git 'https://github.com/abhishpj/DataBase.git'
      },
      Protocol : {
        git 'https://github.com/abhishpj/Protocol.git'
      },
      UI : {
        git 'https://github.com/abhishpj/UI.git'
      }
    )
  }
}


stage('run-parallel-branches') {
  steps {
    parallel(
      Database: {
        sh ''' 
              cd DataBase
                bash prcs.sh '''

      },
      Protocol : {
        sh ''' git clone https://github.com/dprabhua/Protocol.git
                cd Protocol
                bash proc.sh '''
      },
      UI : {
        bat label: 'abc', script: 'abc.bat'
      }
    )
  }
}


  }
}
