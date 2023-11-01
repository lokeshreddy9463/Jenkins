pipeline {
	agent any
  stages{
    stage('Checkout') {
        checkout scm
    }

    stage('Build') {
    	when{
		expression{
			BRANCH_NAME == '1-scripted' || BRANCH_NAME == 'main'
		}
	}
	echo "Hi from build block"
    
    }

    post 
    {
    	echo "Hi from post block"
	always {
		echo "Hi from always block"
	}
	success{
	echo "Hi from success block"
	}
  } 
  }
}

