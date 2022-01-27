pipeline {
    
    agent any  // sirve para definir donde se quiere ejecutar la tarea (any, en cualquier sitio)
	
	stages {
	    stage("Etapa 1"){
	        steps{                             // hacemos las llamadas a los plugins
	            sh "echo Soy la Etapa 1"    
	            sh "echo sigo en la Etapa 1"
	            sh "echo acabo la Etapa 1"
	       }
	       post{                 // postareas
	           always {           //* postareas que se ejecutan siempre
	               sh "echo la Etapa 1 se ejecutó"  // llamada al plugin que ejectua una Shell
	           }
	           success {          //* postareas si acaba bien
	               sh "echo la Etapa 1 acabó que te cagas"
	           }
	           failure {           // postareas si falla
	               sh "echo la Etapa 1 cascó"
	           }
	           
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
   post{                 // postareas
       always {           //* postareas que se ejecutan siempre
           sh "echo todo se ejecutó"  // llamada al plugin que ejectua una Shell
       }
       success {          //* postareas si acaba bien
           sh "echo todo acabó que te cagas"
       }
       failure {           // postareas si falla
           sh "echo algo cascó"
       }
	           
   }
}
