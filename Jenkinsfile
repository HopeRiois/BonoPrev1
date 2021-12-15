pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven 3.8.4"
    }
    stages {
        stage('clean') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true clean"
            }
        }
        stage('test') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true test"
            }
        }
        stage('package') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true package"
            }
        }
    }
}
