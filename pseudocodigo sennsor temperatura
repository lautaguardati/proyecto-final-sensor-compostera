    INICIO
PROCEDIMIENTO InicializarPines()
FINPROCEDIMIENTO

PROCEDIMIENTO DescargarCapacitor()
  Esperar(10 * TAU)
FINPROCEDIMIENTO

PROCEDIMIENTO CargarCapacitor()
FINPROCEDIMIENTO

FUNCION ObtenerTemperatura(tiempo_delta)
  temperatura = BuscarEnTablaDeValores(tiempo_delta)
  RETORNAR temperatura
FINFUNCION

PROCEDIMIENTO Reportar(temp)
  Imprimir("La temperatura actual es: " + temp)
FINPROCEDIMIENTO



  InicializarPines()

  DescargarCapacitor()

  MIENTRAS (VERDADERO) HACER
    
    CargarCapacitor()
    start_time = time.ticks_us() 

    MIENTRAS (leer_pin_sensor() == 0) HACER
    FIN MIENTRAS

    end_time = time.ticks_us()

    delta_t = time.ticks_diff(end_time, start_time)

    temperatura = ObtenerTemperatura(delta_t)

    Reportar(temperatura)

    DescargarCapacitor()
    Esperar(10 * TAU)

    time.sleep(15) 

  FIN MIENTRAS

FIN
