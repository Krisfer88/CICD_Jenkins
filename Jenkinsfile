import java.text.SimpleDateFormat
def fechaActual = new Date()
def formato = new SimpleDateFormat("EEEE", new Locale("es"))
def diaSemana = formato.format(fechaActual)

pipeline
{
    agent any
    tools
    {
        maven 'Maven'
        jdk 'JAVA'
    }    
    stages
    {
        stage("Valicacion de dia de la semana para hacer acciones")
        {
            steps
            {
                script
                {
                    echo "Hoy es el dia  "+ diaSemana
                    if (diaSemana == "miercoles")
                    {
                        def tiempo = "Soleado"
                        echo "El tiempo actual es: " + tiempo
                    }
                    if (diaSemana == "jueves")
                    {
                        echo "Clonado del repo de la rama main "
                        git branch: "main", url: "https://github.com/Krisfer88/CICD_Jenkins.git"
                    }
                    if (diaSemana == "lunes")
                    {
                        echo "NO se hace un carajo"
                    }
                    if (diaSemana == "viérnes")
                    {
                        echo "NO se hace un carajo"
                    }
                    
                }
                
            }
        }
    }
    post
    {
        failure
        {
            echo "El pipeline ha fallado estrepitosamente"
            mail to: 'c.curipallo.zapata@gmail.com', subject: "El pipeline ha fallado estrepitosamente", body:"El pipeline ha fallado estrepitosamente."
        }
    }
}
