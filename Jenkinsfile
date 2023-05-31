import java.time.LocalDate
import java.time.DayOfWeek

// Obtener la fecha actual
def fechaActual = LocalDate.now()

// Obtener el día de la semana de la fecha actual
def diaDeLaSemana = fechaActual.getDayOfWeek()

// Imprimir el día de la semana
println "Día de la semana: ${diaDeLaSemana}"

// Obtener el nombre completo del día de la semana
def nombreCompleto = diaDeLaSemana.getDisplayName(DayOfWeek.FULL, Locale.getDefault())

// Obtener el nombre abreviado del día de la semana
def nombreAbreviado = diaDeLaSemana.getDisplayName(DayOfWeek.SHORT, Locale.getDefault())

// Imprimir los nombres
println "Nombre completo del día de la semana: ${nombreCompleto}"
println "Nombre abreviado del día de la semana: ${nombreAbreviado}"
