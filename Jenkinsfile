pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	
	stages{
		stage('Checkout'){
			steps{
				git branch:'main',url:'https://github.com/chinmayiii/Mymavensel.git'
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean install'
			}
		}
		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}
		
}
		
	}
	
	post {
        success {
            echo "Open SauceDemo: https://www.saucedemo.com"
        }

        failure {
            echo "Build FAILED"
        }
    }
}
