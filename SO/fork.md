# Fork

- PCB (process control block) en el kernel (para almacenar info de nuevo proceso).
- Crea espacio de direccionamiento para nuevo proceso.
- Copia el espacio de direccionamiento del padre en el espacio creado para el hijo.
- Hijo hereda recursos del padre.
- Carga espacio de dir de nuevo proceso en memoria.
- SO ahora puede ejecutar nuevo proceso.
- fork() es implementado por llamadas al sistema [[clone]]().