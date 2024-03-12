pipeline {
    agent any
    stages {
        stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage("Clone Repo"){
            steps{
                sh "git clone https://github.com/jenkins-docs/simple-java-maven-app.git"
            }
        }
        stage("Build"){
            steps{
                dir("simple-java-maven-app"){
                    sh "mvn clean install"
                }
            }
        }
        stage("Test"){
            steps{
                dir("simple-java-maven-app"){
                    sh "mvn test"
                }
            }
        }
    }
}




// pipeline {
//     agent any

//     stages {
//         stage('Hello') {
//             steps {
//                 echo 'Hello World'
//                 git credentialsId: '18de854f-d9bf-437f-b94b-9797ca3ded2f', url: 'https://github.com/shivmodi1203/simple-java-maven-app.git'
//             }
//         }
//     }
// }
