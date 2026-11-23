# Monitor de los sitios

Revisa cada 10 minutos, desde GitHub Actions, que **devolta.com.co** y **contrataylicita.co** respondan, que sus
certificados no estén por vencer y que la descarga diaria de SECOP II de Contrata y Licita siga llegando.

Si algo falla dos veces seguidas, abre un issue **«Falla en los sitios»** y marca la ejecución en rojo (GitHub envía el correo «Run failed»; como
correo). Mientras siga la falla agrega un comentario por hora como máximo; cuando todo vuelve a responder, lo cierra.

- Qué se revisa: la lista y los umbrales están en `.github/workflows/monitor.yml`.
- Secreto `ANON_CYL`: la llave pública (anon) de Supabase de Contrata y Licita, la misma que va en la página.
- Correr a mano: pestaña Actions → «Monitor de los sitios» → Run workflow.

Es público para no gastar los minutos de GitHub Actions de los repositorios privados; no contiene datos ni secretos.
