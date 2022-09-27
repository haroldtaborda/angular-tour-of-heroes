pipeline {
    agent any
    
    tools {
        nodejs "nodejs"
    }
   stages { 
    stage('Install') {
        steps {
          sh "npm install"
        }
      }
      stage('Analisis') {
        steps {
          sh "npm run ng lint"
        }
    }
     stage('Test') {
        steps {
         sh "npm run test --watch=false"
        }
    }
       stage('Build') {
        steps {
            sh "npm run  ng build"
        }
    }
      stage('Artifactory') {
        steps {
          sh "npm install"
        }
    }
      stage('Deploy') {
        steps {
          sh "npm install"
        }
    }
    
   }    
}
