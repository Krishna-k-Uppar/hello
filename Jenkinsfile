pipeline { 
    agent any 

    tools { 
        maven 'Maven' // Ensure this matches the Maven tool name configured in Jenkins
    } 

    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'main', url: 'https://github.com/Krishna-k-Uppar/hello.git'

            } 
        } 

        stage('Build') {  
            steps { 
                bat 'mvn clean package'  
            } 
        } 

        stage('Test') {  
            steps { 
                bat 'mvn test'  
            } 
        } 

       stage('Run Application') {  
           steps { 
              bat 'java -jar target\\Hello2-0.0.1-SNAPSHOT.jar'

              }
         }
     } 
}
