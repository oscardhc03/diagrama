```mermaid
graph TD

subgraph MAL("Middleware Abstraction Layer (MAL)")
    subgraph GPIO
        GPIO.c
        GPIO.h
    end
    subgraph DAC
        DAC.c
        DAC.h
    end
    subgraph RGB_LED
        RGB_LED.c
        RGB_LED.h
    end
    subgraph PIT
        PIT.c
        PIT.h
    end
    subgraph NVIC
        NVIC.c
        NVIC.h
    end
    subgraph Watchdog
        Watchdog.c
        Watchdog.h
    end
end

subgraph Control("Capa de Control de Visualización y Pantalla")
    subgraph Display
        Display_Segments.c
        Display_Segments.h
    end
    subgraph Digital_Clock_Control
        Digital_Clock_Control.c
        Digital_Clock_Control.h
    end
    subgraph Display_Error
        Display_Error.c
        Display_Error.h
    end
end

subgraph Logic("Capa de Lógica de Aplicación")
    subgraph Clock
        Clock.c
        Clock.h
    end
    subgraph Stopwatch
        Stopwatch.c
        Stopwatch.h
    end
    subgraph Alarm
        Alarm.c
        Alarm.h
    end
    subgraph Config_Time
        Config_Time.c
        Config_Time.h
    end
end

subgraph UI("Capa de Interfaz de Usuario (UI)")
    subgraph Main
        Main.c
        Main.h
    end
end
