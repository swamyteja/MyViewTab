pipeline {
agent any
    stages {
        stage('Compile') {
            steps {
               echo 'Compiling the Plugin'
	     bat 'atlas-compile'
            }
        }

        stage('Packaging') {
steps{
              echo 'Packaging the Plugin'
          bat 'atlas-package'
        }
}
        stage('Deploying') {
steps{

 

echo 'deploy started'
bat 'atlas-install-plugin --username sridurgaswamyteja --password Teja7c119 --server localhost --http-port 8082 --plugin-key com.atlassian.jira.jira-api --context-path "" '
}

        }

    }
}