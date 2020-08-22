def region = 'us-west-2'

pipeline {
    agent any
    
    parameters {
      string(name: 'EnvName', defaultValue: 'some-value', description: 'Some sample name')
    }
    
    environment {
    ENV    = "${params.EnvName}"
    REGION = "${region}"

    }
    stages {
        stage('build') {
            steps {
                echo "Hello World!"
                sh """
                      #!/bin/bash
                      
                      aws s3 ls;
                      echo "TF Version checking...."
                      terraform -v
                   """
            }
        }
    }
}
