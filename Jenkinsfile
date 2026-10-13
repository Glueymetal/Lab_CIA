pipeline {
    agent any

    tools{
        maven 'Maven'
    }

    stages {

        stage('Checkout')
        {
            steps{
                checkout scm
            }
        }

        stage('Clean and Test') {
            steps {
                bat 'mvn clean test'
            }
            post {
                always {
                    junit 'course-registration-app/target/surefire-reports/TEST-*.xml'
                }
            }
        }

        stage('Package') {
            steps {
                bat 'mvn package -DskipTests'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts(
                    artifacts: 'course-registration-app/target/*.jar',
                    fingerprint: true
                )
            }
        }

        }

        post {
            success {
                echo 'Success'
            }
            failure{
                echo 'Failure'
            }
            always{
                echo 'Execution finished'
            }
        }
    }
