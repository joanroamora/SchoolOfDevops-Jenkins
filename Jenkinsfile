pipeline {
    agent {
        docker { 
            image 'node:18.10-bullseye'
            args '-p 3000:3000'
        }
    }
        stages {
            stage('Build') {
                steps {
                    sh 'echo "HELLOWORLD"'
                    sh 'npm install'
                }
            }
            
            stage('Test') {
                steps {
                    echo 'Testing..'
                }
            }
            
            stage('Packaging') {
                steps {
                    echo 'Packaging..'
                    //sh 'mkdir /home/augustus/Desktop/testeo/artifacts'
                    archiveArtifacts artifacts: '*.*', fingerprint: true 
                    //sh 'cp -R /var/lib/jenkins/workspace/SoD-jp-02 /home/augustus/Desktop/testeo/artifacts'
                }
            }
            
            stage('Deploy') {
                steps {
                    echo 'Deploying'
                    sh 'ls -a && cd artifacts && ls -a'

                }
            }
            
            // stage('Deploy') {
            //     steps {
            //         echo 'Deploy'
            //         sh 'docker pull jeisonroa1/image:1 ; docker run --name contenedor -d -p 8001:8001 jeisonroa1/image:1 npm start'
            //        input "Presione una tecla para detener el servidor."
            //        sh 'docker stop contenedor; docker rm -f contenedor ; docker rmi -f jeisonroa1/image:1'

            //     }
            // }
            
            
                  
        }
} 
