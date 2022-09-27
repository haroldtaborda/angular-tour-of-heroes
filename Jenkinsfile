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
      stage('Analicis') {
        steps {
       sh "ng lint"
        }
    }
     stage('Test') {
        steps {
       sh "npm run test --watch=false"
        }
    }
        stage('Build') {
        steps {
       sh "npm build --prod
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
