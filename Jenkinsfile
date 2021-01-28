pipeline {
    agent any
    environment {
        PATH = "C:\maven\bin\:$PATH"
    }
    stages {
        stage("clone code"){
            steps{
               git clone https://github.com/mnreddy69/jf.git
            }
        }
        stage("build code"){
            steps{
              bat "($PATH)/mvn clean install"
            }
        }
        stage("deploy"){
            steps{
              copy "C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\jf\target\webapp.war  C:\tomcat\webapps\webapp.war"
             }
        }
    }
}
