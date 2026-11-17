# camarahiperbarica-web

Sitio de **Cámara Hiperbárica** (https://camarahiperbarica.mx): oxigenación hiperbárica en la Col. Del Valle, CDMX. Parte de Grupo Empresarial Díaz.

Es un sitio estático (HTML, CSS y JavaScript, sin compilación).

## Estructura

```
index.html                 Página de inicio
aviso-de-privacidad.html   Aviso de privacidad
404.html                   Página de error
beneficios.html            Redirige a /#tratamientos (página del sitio anterior)
pacientes.html             Redirige a /#tratamientos (página del sitio anterior)
contacto.html              Redirige a /#cita (página del sitio anterior)
css/styles.css             Estilos
js/config.js               Número de WhatsApp (editar aquí)
js/main.js                 Menú, pestañas, preguntas frecuentes y formulario
robots.txt, sitemap.xml    SEO
```

Las imágenes (`img/logo.png`, `img/bg.jpg`, `img/f1.jpg`, `img/f6.jpg`, `img/f7.jpg`) ya están en el hosting y el sitio las usa tal cual.

## Datos de contacto usados
- Luz Saviñón 509, Del Valle Centro, Benito Juárez, 03103 CDMX
- Citas: 55 3501 0034 · WhatsApp: 55 5207 8070 (en `js/config.js`)
- contacto@camarahiperbarica.mx
- Lunes a sábado, 9:00 a 17:00

## Pendientes
- Nombre y cédula profesional del médico responsable (recomendado mostrarlos junto a "Supervisión médica").
- Duración de cada sesión y número típico de sesiones.
- Precios de valoración, sesión y paquetes (hoy los botones piden el precio por WhatsApp).
- Testimonios reales con autorización escrita del paciente.
- Seguros aceptados y facturación.
- Aviso de responsable sanitario / COFEPRIS si aplica.
- Revisar el aviso de privacidad con asesoría legal (el formulario recaba datos de salud).

## Lenguaje médico
El texto presenta la terapia como **tratamiento complementario con valoración médica previa** y evita prometer resultados. Antes de agregar afirmaciones de eficacia, confirmarlas con el médico responsable y con fuentes.

## Publicación
Cada cambio en `main` se publica por FTP (`.github/workflows/deploy.yml`) con los secrets `FTP_SERVER`, `FTP_USERNAME`, `FTP_PASSWORD` y `FTP_SERVER_DIR` de este repositorio. Antes de subir, el flujo guarda un respaldo de las páginas que reemplaza en los *Artifacts* de cada ejecución (90 días).

## Probar en tu computadora

```
python3 -m http.server 8000
```

y entra a http://localhost:8000.
