pipeline {
  agent any

  stages {

stage('run-parallel-branches') {
  steps {
    parallel(
      Database: {
        sh ''' git clone https://github.com/dprabhua/DataBase.git
                cd DataBase
                bash prcs.sh '''

      },
      Protocol : {
        sh ''' git clone https://github.com/dprabhua/Protocol.git
                cd Protocol
                bash proc.sh '''
      },
      UI : {
        sh ''' git clone https://github.com/abhishpj/UI.git
               cd  UI
                bash process.sh '''
      }
    )
  }
}


  }
}
