pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
    }
    stages {
        stage('SCM checkout') {
            steps {
                git "git@bitbucket.org:allanchangcl/clchangnet-tests.git"
        }
    }

         stage('Build') {
             steps {
                sh 'mvn --version'
                sh "mvn clean package"
        }
    }

          stage('Compile') {
              steps {
                dir("target") {
                    sh "java -jar standalone-clchangnet-tests.jar"
                }
        }
    }

  }

}
