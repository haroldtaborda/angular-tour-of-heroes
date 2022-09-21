pipeline {
    agent any
    
    tools {
        nodejs "nodejs"
    }
   stages { 
    stage('Build') {
        steps {
          sh "npm install"
           sh "npm run ng build"
        }
      }
     stage('Test') {
        steps {
       
        }
    }
      stage('Deploy') {
        steps {
          sh "npm start"
        }
    }
    
   }    
}
