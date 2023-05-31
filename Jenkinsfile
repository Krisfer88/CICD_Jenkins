pipeline {
    agent any
    
    stages {
        stage('Check Day of Week') {
            steps {
                script {
                    def currentDate = new Date()
                    def dayOfWeek = currentDate.format('EEEE', new Locale('es', 'ES'))
                    
                    if (dayOfWeek == 'martes') {
                        echo "El usuario ejecutando el PPL es ${env.USERNAME}"
                    } else if (dayOfWeek == 'miercoles') {
                        def weather = obtenerEstadoDelTiempo()
                        echo "El estado del tiempo actual es: ${weather}"
                    } else if (dayOfWeek == 'jueves') {
                        checkout scm
                        echo "Repositorio clonado y rama principal obtenida"
                    } else if (dayOfWeek == 'viernes') {
                        echo "No se realizará ninguna acción hoy (viernes)"
                    } else if (dayOfWeek == 'lunes') {
                        echo "No se realizará ninguna acción hoy (lunes)"
                    }
                }
            }
        }
    }
}
