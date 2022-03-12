pipeline {
    
    agent any


    tools {
    jdk 'Java8'
    maven 'Maven3.3.9'

  }

    stages {
        
        stage('Git Clone') {
            steps {
                // Get some code from a GitHub repository
               git branch: 'main',
               url: 'https://github.com/sowmya2506/apache1.git'
            }

        }
        stage('aws') {
            steps {
                // Get some code from a GitHub repository
                sh  '''
                  cd $WORKSPACE
                  aws s3 sync . s3://sowmya-2506
                  '''

            }
        }
      }
     }
