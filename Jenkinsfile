pipeline {
    
    agent any  // sirve para definir donde se quiere ejecutar la tarea (any, en cualquier sitio)
	
	stages {
	    stage("Etapa 1"){
	        steps{                        // hacemos las llamadas a los plugins
	            sh "echo Soy la Etapa 1"  // llamada al plugin que ejectua una Shell
	       }
	    }
        stage("Etapa 2"){
            steps{
            sh """
            echo Soy la Etapa 2
            echo Acabo la Etapa 2
            """
            }
        }
    }
}
