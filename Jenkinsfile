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
                when {
              expression {
                currentBuild.result == null || currentBuild.result == 'SUCCESS' 
              }
            }
                steps {
                    sh 'echo ""Build succesfully, deploy succesfully.'
                }
            } 
         
        }
} 
