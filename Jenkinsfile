import java.text.SimpleDateFormat
import java.util.Date
import java.util.Locale

pipeline {
    agent any
    
    stages {
        stage('Check Day of Week') {
            steps {
                script {
                 date = new Date()
                 format = new SimpleDateFormat("EEEE", new Locale("es", "ES"))
                 formattedDate = format.format(date)
                    echo "El dia de hoy es " + formattedDate
                    if (formattedDate == "miercoles"){
                        echo "Conchatumadre " + formattedDate
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
