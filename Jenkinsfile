pipeline {
    agent any
	
	tools{
		maven 'maven 3.6.1'
	}

    stages{
        stage("build"){
            steps{
                echo 'Compiling worker app'
				dir('worker'){
					sh 'mvn compile'
				}
            }
        }
        stage("test"){
            steps{
                echo 'Running Unit Tests on worker app'
            }
        }
        stage("package"){	
			steps{
				echo 'Packaging worker app'
			}
		}
    } 

    post{
      always{
          echo 'Building multibranch pipeline for worker is completed...'
      }
    }
}
