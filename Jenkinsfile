pipeline {

    agent any

     
    stages {
        
        stage ('checkout'){
            steps {
            git  'https://github.com/hsindia2020/jpetstore-6.git'
            }
        }

        stage ('test') {

            steps {

             //       sh 'echo "hello"'
                   // sh './mvnw test'
sh './mvnw clean'
            }

         }       

        stage ('package') {

            steps {


                    sh './mvnw clean package'

            }

         }
        stage ('sonar') {

            steps {


                    sh '/opt/apps/sonar-scanner-4.6.0.2311-linux/bin/sonar-scanner -X'

            }

         }     
        
        
     
        

    }
}
