pipeline {
    agent any
    stages {
        stage ('git job') {
            steps {
                echo "cloning....."
            }
        }
        stage ('build job') {
            steps {
                echo "building....."
                sh 'mvn compile'
            }
        }
        stage ('testjob') {
            steps {
                echo "testing....."
                sh 'mvn test'
            }
        }
        stage ('deployjob') {
            steps {
                echo "deployiing....."
                sh 'mvn install'
                archiveArtifacts artifacts: 'target/addressbook.war', followSymlinks: false
            }
        }     
    }
}
