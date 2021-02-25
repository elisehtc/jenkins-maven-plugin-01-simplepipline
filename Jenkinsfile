pipeline{
    agent any
    stages{
        stage("Checkout Code from SCM"){
            steps{
                git url: "https://gitlab.com/mromdhani/07-jenkins-maven-plugin-01-unit-and-integration-tests.git",
                branch: 'master'
            }            
        }
         stage("Clean Up"){
            steps{
               sh 'mvn clean';
            }            
        }
        stage("Compile it "){
            steps{
               sh 'mvn compile';
            }            
        }
        stage("Unit Tests "){
            steps{
               sh 'mvn test';
            }            
        }
         stage("Package (i.e. Generale the deployable JAR)"){
            steps{
               sh 'mvn compile'
            }            
        }
    }
   
}