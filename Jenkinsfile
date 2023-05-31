import java.text.SimpleDateFormat
import java.util.Calendar

def obtenerDiaActual() {
    // Obtener una instancia del calendario actual
    def calendario = Calendar.getInstance()
    
    // Obtener el día del mes actual
    def dia = calendario.get(Calendar.DAY_OF_MONTH)
    
    // Obtener el mes actual (ten en cuenta que en Calendar el mes comienza en 0)
    def mes = calendario.get(Calendar.MONTH) + 1
    
    // Obtener el año actual
    def anio = calendario.get(Calendar.YEAR)
    
    // Formatear la fecha como una cadena
    def formato = new SimpleDateFormat("dd/MM/yyyy")
    def fechaActual = formato.format(calendario.getTime())
    
    // Imprimir la fecha actual
    println "Día actual: $dia"
    println "Mes actual: $mes"
    println "Año actual: $anio"
    println "Fecha actual: $fechaActual"
}

obtenerDiaActual()
