pipeline {
    agent any   
    stages {
        stage(' dockerhub login') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'DHCred', passwordVariable: 'pass', usernameVariable: 'user')]){
                    sh 'docker login -u ravisingh123 -p ${pass}'
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


                


                
