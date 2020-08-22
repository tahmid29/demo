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
            }
        }
    }
}
