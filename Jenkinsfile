import java.text.SimpleDateFormat
import java.util.Date
import java.util.Locale

pipeline {
    agent any
    
    stages {
        stage('Check Day of Week') {
            steps {
                script {
                def date = new Date()
                def format = new SimpleDateFormat("EEEE", new Locale("es", "ES"))
                def formattedDate = format.format(date)
                    
                    if (formattedDate == 'martes') {
                        echo "El usuario ejecutando el PPL es ${env.USERNAME}"
                    } else if (formattedDate == 'miércoles') {
                        def weather = "Soleado"
                        echo "El estado del tiempo actual es: ${weather}"
                    } else if (formattedDate == 'jueves') {
                        checkout scm
                        echo "Repositorio clonado y rama principal obtenida"
                    } else if (formattedDate == 'viernes') {
                        echo "No se realizará ninguna acción hoy (viernes)"
                    } else if (formattedDate == 'lunes') {
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
