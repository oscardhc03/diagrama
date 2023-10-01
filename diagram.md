```mermaid
graph TD

    %%Capa de hardware%%
    GPIO("GPIO")
    DAC("DAC")
    RGB_LED("RGB_LED")
    PIT("PIT")
    NVIC("NVIC")
    Watchdog("Watchdog")

    %%Capa de control de visualización y pantalla%%
    Display("Control de visualización y pantalla")
    Config_Time("Configuración de la hora")
    Alarm("Alarma")
    Stopwatch("Cronómetro")
    Clock("Reloj")

    %%Capa de lógica de aplicación%%
    Logic("Lógica de aplicación")
    Main("Main")

    %%Capa de interfaz de usuario%% (UI)
    UI("Interfaz de usuario")

    %%Conexiones%%
    GPIO --> Display
    DAC --> Display
    RGB_LED --> Display
    PIT --> Display
    NVIC --> Display
    Watchdog --> Display
    Display --> Logic
    Logic --> Main
    Logic --> UI

    %%Estilos%%
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
