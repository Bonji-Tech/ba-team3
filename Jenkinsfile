pipeline {
    agent any
        stages{
            stage('1-Clone Repo'){
                steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'gitub-id', url: 'https://github.com/Bonji-Tech/ba-team3.git']]])
                }
            }            
            stage('1-script-make a left'){
                steps{
                sh 'bash -x /var/lib/jenkins/workspace/$project/directions.sh'
                sh 'cat /etc/passwd'
                }
            }
            stage('2-make a right'){
                steps{
                sh 'echo "walk.."'
                sh 'lscpu'
                }
            }
            stage('3-make another left'){
                steps{
                sh 'echo "walk..."'
                sh 'cat /etc/passwd | grep ubuntu'
                }
            }
            stage('4-cross the street'){
                steps{
                sh 'echo "walk..."'
                sh 'whoami'
                }
            }
        }
}