pipeline {
    agent {
        docker { image 'node:16.13.1-alpine' }
    }
        stages {
            stage('Prepare') {
                steps {
                    echo 'Preparing...'
                    sh 'apk add bash'
                    sh 'echo "HELLOWORLD"'
                    sh 'bash script.sh'
                }
            }
            
            // stage('Build') {
            //     steps {
            //         echo 'Building..'
            //         sh 'cd CICD; docker build . -t jeisonroa1/image:1 '

            //     }
            // }
            
            // stage('Test') {
            //     steps {
            //         echo 'Testing..'
            //         sh 'docker run --name contenedor -d jeisonroa1/image:1 npm test'

            //     }
            // }
            
            // stage('Push') {
            //     steps {
            //         echo 'Clean & Push'
            //         sh 'docker rm -f contenedor ; docker login -u jeisonroa1 -p jenkins ; docker push jeisonroa1/image:1 ; docker rmi -f jeisonroa1/image:1 '

            //     }
            // }
            
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
