def fecha = new Date()
def formatoFecha = new java.text.SimpleDateFormat("yyyy-MM-dd HH:mm:ss")
def fechaFormateda = formatoFecha.format(fecha)
pipeline
{
    agent any
    environment
    {
        int clima_actual = 21
        int poblacion_actual = 80000
        neto = 0.8
        
        
    }
    stages
    {
        stage("Bienvenido")
        {
            steps
            {
                script
                {
                def saludo = "Bienvenido la fecha actual es:" + fechaFormateda
                def contenido = saludo
                println saludo
                }
            }
        }
        
        stage("Informacion relevante sobre tu ciudad actual")
        {
            steps
            {
                script
                {
                    def info = "El clima actual de tu ciudad es de " + clima_actual + " grados"
                    def poblacion = "La poblacion actual es " + poblacion_actual + " habitantes"
                    println info
                    println poblacion
                }
            }
        }
        
        stage("Poblacion Neta")
        {
            steps
            {
                script
                {
                    poblacion_neta = poblacion_actual.toInteger()  * neto.toDouble()
                    println "La población neta es " + poblacion_neta 
                }
            }
        }
        
        stage("Genercion fichero salida")
        {
            steps
            {
                script
                {
                    def contenido = "El clima actual de tu ciudad es de " + clima_actual + " grados" + " con poblacion actual de " + poblacion_actual + "\nLa poblacion neta es " + poblacion_neta
                    writeFile(file: "ejercicio_2.txt", text:contenido)
                    println contenido
                }
            }
        }
    }
}
