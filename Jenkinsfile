pipeline {
  agent any
  stages {
    stage('Stage1') {
      agent any
      environment{
          LOG_LEVEL = 'INFO'
      }
      steps {
        echo 'Building Release ${RELEASE} With Log_Level ${LOG_LEVEL} ....}'
      }
    }
    
    stage('Test') {
      steps {
        echo 'Building Release ${RELEASE} With Log_Level ${LOG_LEVEL} is not visible....}'
      }
    }

  }
  environment {
    ReLEASE = 20.05
  }
}
