pipeline{
    agent any
    tools{
        maven 'maven3.9
    }
    stages{
        stage("checkout_code"){
            staps{
                gitbranch:'master' , url: 'https://github.com/AnuMoharana802/java-web-app.git'
            }
        }
        stage("Build_code"){
            stage {sh'mvn clean package'
        }
    }
    stage("Deployment"){
        steps {
            deploy adapters:[tomcat9(credentialsd:'tomcat',url:'http://16.171.14.216:8080/')],contextpath:'welcomeapp',war:'**/*.war'
            }
    }
}