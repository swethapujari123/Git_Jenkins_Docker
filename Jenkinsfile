pipeline {
    agent any

    environment {
        CONTAINER1 = "container1"
        CONTAINER2 = "container2"
        CONTAINER3 = "container3"
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Deploy app1') {
            steps {
                sh '''
                docker cp app1.html $CONTAINER1:/usr/local/tomcat/webapps/ROOT/index.html
                '''
            }
        }

        stage('Deploy app2') {
            steps {
                sh '''
                docker cp app2.html $CONTAINER2:/usr/local/tomcat/webapps/ROOT/index.html
                '''
            }
        }

        stage('Deploy app3') {
            steps {
                sh '''
                docker cp app3.html $CONTAINER3:/usr/local/tomcat/webapps/ROOT/index.html
                '''
            }
        }
    }
}
