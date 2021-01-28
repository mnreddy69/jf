pipeline {
    agent any
    environment {
        PATH = "/opt/apache-maven-3.6.3/bin:$PATH"
    }
    stages {
        stage("clone code"){
            steps{
               git credentialsId: 'git_credentials', url: 'https://github.com/mnreddy69/jf'
            }
        }
        stage("build code"){
            steps{
              sh "mvn clean install"
            }
        }
        stage("deploy"){
            steps{
              copy "C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\jf\target\webapp.war  C:\tomcat\webapps\webapp.war"
             }
        }
    }
}
