pipeline{
    
    agent any
    tools { maven "M3"}
    stages{
        stage("check out"){
            steps{
                git branch : "main" , url :  "https://github.com/AnjuMeleth/SpringPetClinic.git"
            }
        }
        stage("build"){
            steps{
              sh "mvn compile"  
            }
            
        }
        stage("test"){
            steps{
                sh "mvn test"
            }
        }
        stage("package"){
            steps{
                sh "mvn package"
            }
        }
        stage("deploy"){
            steps{
                sh "java -jar /home/coder/.jenkins/workspace/petClinicDeclerativePipeline/target/*.jar"
            }
        }
    }
}
