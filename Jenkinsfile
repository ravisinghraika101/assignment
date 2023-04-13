pipeline {
    agent any   
    stages {
        stage(' dockerhub login') {
            steps {
                withCredentials([usernamePasswod(credentialsId:'DockerCred', passwordVariable: 'ravi1234', username: 'ravisingh123')]){
                sh 'docker login -u $ravisingh123 -p $ravi1234'
            }
        }
        }
        stage('Build Image') {
             steps {
                  sh  'docker build -t assignment-image . '
             }
        }
        stage ('Push Image') {
             steps {
                   sh '''
                      docker tag assignment-image ravisingh1234/assignment-image:tagname
                      docker push ravisingh1234/assignment-image:tagname
                       '''
                    }
                }
            }
}


                


                
