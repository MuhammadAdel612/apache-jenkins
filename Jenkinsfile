pipeline {
    agent any
    
   
   stages {
       stage ('git checkout') {
           steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']],userRemoteConfigs: [[url: 'https://github.com/MuhammadAdel612/apache-jenkins.git']]])
           }
       }
      
       

       
       stage ('Deploy to Cluster') {
            steps {
                sh "oc apply -f maven-deploy.yml"
                }
            }
}
}
