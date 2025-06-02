# ACTIVIDAD 1  
## UNIDAD 1  
**MATERIA:** HACKING  ÉTICO 

**ALUMNA:** DIAZ BARRERA KARLA

**GRUPO:** IRIYC91

### Informe de Pruebas de Seguridad.
Entorno de pruebas: Mutillidae II (entorno local). 
Herramienta utilizada: Burp Suite. Navegador: Chromium integrado en Burp. 

Objetivo: Análisis del tráfico HTTP y detección de fallos en el control de sesiones y validación de entradas.
--  

---

### Actividades elaboradas:  

Desarrollo de la actividad:
La actividad comenzó con la configuración de Burp Suite , enfocándose en habilitar la interceptación del flujo de datos entre el cliente (navegador) y el servidor. Desde el apartado Proxy , se revisaron los ajustes de conexión para asegurarse de que el tráfico pasará a través de localhost, utilizando la configuración estándar para redes locales.

Se activó la opción Interceptar respuestas del servidor , lo que permitirá observar no solo las solicitudes salientes, sino también las respuestas generadas por el servidor. Posteriormente, se utilizó la función Open Browser para abrir un navegador integrado con Burp.

![Image](https://github.com/user-attachments/assets/0e4fac0e-9f20-45e2-bc86-8efbf9ba7e8c)



Usando el navegador de Burp Suite, se ingresó a la aplicación local a través de localhost . Navegando por el menú de OWASP 2017 > SQL Injection > SQL Insert Injection > Register,
se accedió a un formulario de registro donde se introdujeron datos ficticios (usuario, contraseña, etc.) para simular un alto de usuario.

![Image](https://github.com/user-attachments/assets/486d4013-1c20-472c-90b0-645a4d2c7077)



Después del registro, se procedió al módulo de inicio de sesión ubicado en:
OWASP 2017 > SQL Injection > SQL Extract Data > User Info.

Antes de enviar el formulario, se activó la función Intercept is on , lo cual permitió que Burp Suite retuviera la solicitud enviada al servidor para su análisis.

![Image](https://github.com/user-attachments/assets/87d29380-2ce7-4d71-9634-5ad71de54f1c)



Durante la inspección del contenido de las solicitudes, se identificó un parámetro llamado uid, el cual representaba el identificador del usuario en sesión (por ejemplo, uid=2para un estándar). Se manipuló dicho valor manualmente para explorar si era posible acceder a privilegios superiores sin autenticación adicional.

Este experimento sirvió como ejemplo práctico de cómo la falta de controles adecuados puede permitir ataques de escalada de privilegios mediante la modificación directa de parámetros en tránsito.

![Image](https://github.com/user-attachments/assets/d18dc91d-a272-41b3-b09c-166a3922a9db) 



⚠️ Advertencia:

Esta práctica fue realizada únicamente con fines educativos, en un entorno de pruebas local.
No debe ejecutarse en sistemas reales sin consentimiento explícito del propietario o fuera de laboratorios autorizados.

# ACTIVIDAD 2
### Actividades elaboradas: 
Aplicación vulnerable: Mutillidae II
Almacenamiento en AlwaysData
### Objetivo 
Demostrar cómo es posible capturar información sensible a través de un archivo PHP malicioso, cargado mediante un formulario vulnerable.

Se creó una cuenta en AlwaysData , que permite utilizar una base de datos MySQL .
Se ejecutó un script SQL para generar una tabla que almacenará la siguiente información:

![Image](https://github.com/user-attachments/assets/6cea137c-ffd1-4bea-893c-62b96fd5bece)

![Image](https://github.com/user-attachments/assets/6cea137c-ffd1-4
Después dbea-893c-62b96fd5bece)

![Image](https://github.com/user-attachments/assets/97f849ab-4587-4115-97dd-43d163e3c376)

![Image](https://github.com/user-attachments/assets/2f202e28-5d36-4867-8637-8600e1d95aee)


# Fin
