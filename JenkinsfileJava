pipeline {

    agent none
    parameters {
    booleanParam(name: 'BUILD', defaultValue: false, description: 'Actually build the program')
  }
    stages {
     when {
        expression { params.BUILD == true}
      }
        stage('RUN MASTER'){
            agent { label 'master'}
            steps {
                sh "javac HelloWorld.java"
                sh "java HelloWorld"
            }
        }
    }
}
