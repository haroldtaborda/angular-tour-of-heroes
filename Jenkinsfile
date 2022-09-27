pipeline {
    agent any
    
    tools {
        nodejs "nodejs"
    }
   stages { 
      stage ('Artifactory configuration') {
            steps {
                rtServer (
                      id: 'ArtifactoryHitos',
                      url: 'http://my-artifactory-domain/artifactory',
                      username: 'admin',
                      password: 'Jfrog2021$$',
                )

                rtNpmResolver (
                    id: "ResolverArtifactoryHitos",
                    serverId: "ArtifactoryHitos",
                    repo: "npm-remote"
                )

                rtNpmDeployer (
                    id: "DeployerArtifactoryHitos",
                    serverId: "ArtifactoryHitos",
                    repo: "npm-local"
                )
            }
        }

    stage('Install') {
        steps {
          sh "npm install"
        }
      }
     stage ('Exec npm install') {
            steps {
                 sh "npm install"
            }
        }
    
   }    
}
