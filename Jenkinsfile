pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                echo "Hello world my testing begins"
            }
            
        }
        stage('Deliver') { 
            steps {
                echo "Snake is delivered" 
            }
        }
    }
}
