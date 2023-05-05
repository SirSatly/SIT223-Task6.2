pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "The project has been built using Maven. The code has been compiled into a .jar file which the computer can run ready to be tested"
            }
        }
        stage('Unit and Intergration Tests') {
            steps {
                echo "Unin testing has been preformed using JUnit to ensure the different parts of the project all work "
                echo "Integration tests have been run to ensure all the different units work together as intended"
            }
            post {
                success {
                    mail to: "hotdelphox@gmail.com"
                    subject: "Unit and Intergration Tests Status"
                    body: "Unit and intergration tests were successful"
                }
                failure {
                    mail to: "hotdelphox@gmail.com"
                    subject: "Unit and Intergration Tests Status"
                    body: "Unit and intergration tests failed"
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo "The code has been analysised using JArchitect to ensure it meets industry standards by checking stuff such as coupling, nesting and complexity"
            }
        }
        stage('Security Scan') {
            steps {
                echo "A security scan has been performed on the project using Snyk to ensure that the are no vulnerabilities in the code"
            }
            post {
                success {
                    mail to: "hotdelphox@gmail.com"
                    subject: "Security Scan Status"
                    body: "Security scan was successful"
                }
                failure {
                    mail to: "hotdelphox@gmail.com"
                    subject: "Security Scan Tests Status"
                    body: "Security scan failed"
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo "Amazon Web Services EC2 has been used to deploy to project to an instance for staging to be able to test in a production like enviroment"
            }
        }
        stage('Intergration Tests on Staging') {
            steps {
                echo "Further intergration tests have been run to ensure all features are still interacting as intended on a production like enviroment"
            }
            post {
                success {
                    mail to: "hotdelphox@gmail.com"
                    subject: "Intergration Tests on Staging Status"
                    body: "Intergration tests on staging were successful"
                }
                failure {
                    mail to: "hotdelphox@gmail.com"
                    subject: "Intergration Tests on Staging Status"
                    body: "Intergration tests on staging failed"
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "The project has been deployed to a production instance of AWS EC2"
            }
        }
    }
}