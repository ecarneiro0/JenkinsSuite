node {
    stage('Test') {
        //Hago un pull del repositorio que contiene el archivo xml del proyecto.
        git credentialsId: 'f9f44c48-c9da-4b14-a494-d81742619c13', url: 'git@github.com:ecarneiro0/SoapSuite.git', branch: 'main'
         
        //Solamente para uso de debug. El objetivo es comprobar que en el directorio del workspace se encuentre copiado el archivo XML de paso anterior.
        bat "dir"
         
        //Ejecutar el testRunner de SoapUI sobre el XML que se encuentra en el proyecto de Jenkins.
        //Se puede poner solamente el nombre del XML porque Jenkins por defecto se encuentra en el lugar donde este archivo será pulleado, si ha sido enviado a otra dirección se debe poner la ruta correspondiente
        bat "C:\\Otrosprogramas\\SmartBear\\SoapUI-5.7.0\\bin\\testrunner.bat -sTestSuite testJenkins-soapui-project.xml"
    }
}