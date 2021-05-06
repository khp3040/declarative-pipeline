pipeline {
  agent any
  stages {
    
    stage('Stage1') {
      agent any
      environment{
          LOG_LEVEL = 'INFO'
      }
      steps {
        echo "Building Release ${RELEASE} With Log_Level ${LOG_LEVEL} ....}"
        
      }
      
    }
    
    
    stage('Test') {
      steps {
        echo "Testing Release ${RELEASE} ....}"
        
      }
      
    }
    
    
    stage('Deploy') {
      input{
       message 'Deploy'
       ok 'Do it'
        parameters{
          string(name: 'TARGET_ENVIRONMENT', defaultValue: 'PROD', description: 'Target Deployment Environment')
          
        }
        
      }
      
       steps {
          echo "Deploying Release ${RELEASE} to Environment ${TARGET_ENVIRONMENT}....}"
        
       }  
      
    } 
    
  }
  
  post{
        always{
          echo 'Prints whether deploy was success or failure ....'
      
        }
      }
  
  
  environment {
    ReLEASE = 20.05
  }
}
