pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                
                    sh 'mvn clean compile'
               
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_3_3') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_3_3') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
