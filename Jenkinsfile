import java.text.DateFormatSymbols

def obtenerDiasSemana() {
    def simbolos = new DateFormatSymbols(new Locale("es"))
    def diasSemana = simbolos.weekdays
    diasSemana = diasSemana.drop(1) // Elimina el primer elemento vacío
    
    return diasSemana
}

def dias = obtenerDiasSemana()
println dias
