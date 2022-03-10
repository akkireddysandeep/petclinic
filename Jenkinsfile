pipeline {
	agent any
    stages {
        stage('Build on k8 ') {
            steps {     
		    withCredentials([file(credentialsId: 'kube_cred', variable: '')]) {
                        sh 'pwd'
                        sh 'cp -R helm/* .'
		        sh 'ls -ltr'
                        sh 'pwd'
                        sh '/usr/local/bin/helm upgrade --install petclinic-app petclinic  --set image.repository=sandeepakkireddy90/petclinic --set image.tag=9'
		    }
            }           
        }
    }
}
