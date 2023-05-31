pipeline {
    agent any
    
    stages {
        stage('Check Day of Week') {
            steps {
                script {
                    def currentDate = new Date()
                    def currentDay = new Date()
                    def dayOfWeek = currentDate.format(java.lang.String, java.util.TimeZone)
                    
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

def obtenerEstadoDelTiempo() {
    // Aquí puedes incluir tu lógica para obtener el estado del tiempo actual
    // Por ejemplo, puedes hacer una llamada a una API de clima
    
    return "soleado"
}
