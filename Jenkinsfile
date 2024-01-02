pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               //bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                //bat "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                 mvn clean -f TicketBookingServiceJunitTesting
            }
        }
        stage('install') {
            steps {
               mvn install -f TicketBookingServiceJunitTesting
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
