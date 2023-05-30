def dia = new Date().getDay()
    def map = [1: 1, 2: 2, 3: 3, 4: 4, 5: 5, 6: 6, 7: 7]
    def tiempo = "lluvioso"
    pipeline{
        agent any
        stages
        {
                stage("mostrar usuario")
                {

                        steps
                        {
                                script
                                    {
                                            echo "Hoy es el dia  " + dia

                                                if (map.get(5) == dia) {

                                                        git branch: "main",
                        url: "https://github.com/asifmj/pruebajenkins"
                                                   
                    }
                                                if (map.get(2) == dia) {
                                                        echo "El usuario que inicio el trabajo es ${env.USERNAME}"
                                                   
                    }
                                                if (map.get(3) == dia) {
                                                        echo "Hoy hace un dia " + lluvioso
                                                   
                    }
                                                if (map.get(1) == dia) {
                                                        echo "Hoy es lunes "  
                                                   
                    }
                                                if (map.get(5) == dia) {
                                                        echo "Hoy es viernes "  
                                                   
                    }
                                       
                }

                           
            }
                   
        }

           
    }
}
