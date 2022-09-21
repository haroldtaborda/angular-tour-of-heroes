pipeline {
    agent any
    
    tools {
        nodejs "nodejs"
    }
   stages { 
    stage('Build') {
        steps {
          sh "npm install"
          sh "ng build"
        }
      }
     stage('Test') {
        steps {
          sh "ng test"
        }
    }
      stage('Deploy') {
        steps {
          sh "npm start"
        }
    }
    
   }    
}
