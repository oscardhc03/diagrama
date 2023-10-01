graph LR
    UI("UI")
    subgraph Lógica
        Logic("Lógica")
        Main("Main")
    end
    subgraph Control_de_visualización_y_pantalla
        MAL("Middleware Abstraction Layer")
        MAL --> Display("Control de visualización y pantalla")
        MAL --> Config_Time("Configuración de la hora")
        MAL --> Alarm("Alarma")
        MAL --> Stopwatch("Cronómetro")
        MAL --> Clock("Reloj")
        subgraph Visualización
            MAL --> Display_Segments("Display de segmentos")
            MAL --> Digital_Clock_Control("Control del reloj digital")
            MAL --> Display_Error("Visualización de errores")
        end
    end
    subgraph Hardware
        MAL --> GPIO("GPIO")
        MAL --> DAC("DAC")
        MAL --> RGB_LED("RGB_LED")
        MAL --> PIT("PIT")
        MAL --> NVIC("NVIC")
        MAL --> Watchdog("Watchdog")
    end
    UI --> Logic
    Logic --> Main
    Logic --> Display
    Display --> Config_Time
    Display --> Alarm
    Display --> Stopwatch
    Display --> Clock
    Display --> Visualización
    Visualización --> Display_Segments
    Visualización --> Digital_Clock_Control
    Visualización --> Display_Error
    Display --> Hardware
    Hardware --> GPIO
    Hardware --> DAC
    Hardware --> RGB_LED
    Hardware --> PIT
    Hardware --> NVIC
    Hardware --> Watchdog
    style UI fill:#e6f2ff
    style Logic fill:#f2f2f2
    style Main fill:#f2f2f2
    style Display fill:#f2f2f2
    style Config_Time fill:#f2f2f2
    style Alarm fill:#f2f2f2
    style Stopwatch fill:#f2f2f2
    style Clock fill:#f2f2f2
    style GPIO fill:#f2f2f2
    style DAC fill:#f2f2f2
    style RGB_LED fill:#f2f2f2
    style PIT fill:#f2f2f2
    style NVIC fill:#f2f2f2
    style Watchdog fill:#f2f2f2
    style MAL fill:#e6f2ff
