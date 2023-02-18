pipeline {
agent any
stages {
    stage('Build') {
        steps {
            sh 'g++ -o PES2UG20CS567-1 hello.cpp'
        }
    }
    
    stage('Test') {
        steps {
            shi './PES2UG20CS567-1'
        }
    }
    
    stage('Deploy') {
        steps {
            // deployment code
            //sh 'mvn deploy'
            echo 'deployment successful'
        }
    }
}

post {
    always {
        script {
            if (currentBuild.result == "FAILURE") {
                echo "Pipeline failed"
            }
        }
    }
}
}
