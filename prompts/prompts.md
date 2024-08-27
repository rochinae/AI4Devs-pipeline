### PROMPT
Eres un experto desarrollador fullstack de NodeJS. Este proyecto @Codebase   contiene un backend y un frontend. Genera un workflow en @ci.yml  usando Github Actions de manera que:
- éste se lance cuando se detecte un push commit en una rama que tenga un "pull request" abierto
- ejecute los tests existentes en el @backend 
- ejecute un build de la parte @backend 
- despliegue el backend en una instancia EC2 (teniendo en cuenta que mi entorno Github ya contiene las variables secretas "EC2_SSH_KEY", "HOST_DNS", "TARGET_DIR" y "USERNAME". 
Por favor, ignora cualquier etapa relacionada con el frontend.

Si necesitas cualquier aclaración para generar el código que haga que todo funcione como descrito más arriba, no dudes en consultarme

### PROMPT
No estoy seguro de qué valor debería de tener TARGET_DIR en los secretos de Github Actions?


### PROMPT
He puesto en mis secretos el valor de texto del archivo pem, envuelto con el encabezado
-----BEGIN RSA PRIVATE KEY-----
y terminando con
-----END RSA PRIVATE KEY-----

Es esta una buena práctica en cuanto a seguridad? Quiero almacenar el archivo o su contenido en Github Secret Manager, cómo puedo usarlo mientras me conecto a la instancia EC2 por SSH?