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
       sh "npm install"
        }
    }
      stage('Deploy') {
        steps {
          sh "npm start"
        }
    }
    
   }    
}
