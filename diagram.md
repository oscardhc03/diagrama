```mermaid
graph LR
title Diagrama por capas con Middleware Abstraction Layer (MAL)

    UI("UI")
    subgraph Lógica
        Logic("Lógica")
        Main("Main")
    end
    subgraph Control de visualización y pantalla
        MAL("Middleware Abstraction Layer")
        MAL --> Display("Control de visualización y pantalla")
        Config_Time("Configuración de la hora")
        Alarm("Alarma")
        Stopwatch("Cronómetro")
        Clock("Reloj")
        subgraph Visualización
            Display_Segments("Display de segmentos")
            Digital_Clock_Control("Control del reloj digital")
            Display_Error("Visualización de errores")
        end
    end
    subgraph Hardware
        GPIO("GPIO")
        DAC("DAC")
        RGB_LED("RGB_LED")
        PIT("PIT")
        NVIC("NVIC")
        Watchdog("Watchdog")
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
