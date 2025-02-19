pieline{

    agent any

    stages{

        stage('build'){

               steps{
                sh 'yarn install'
                sh 'yarn build'
               }
            
        }

        stage('deploy'){

            steps{
            
                sh "pm2 restart note-app || pm2 start yarn --name note-app --start -p 4012"

            }
        }
    }
