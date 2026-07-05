# gastos-viaje

App web de gastos compartidos del viaje (HTML + Firebase).

## Levantar en local

La app es un solo archivo (`gastos-viaje.html`) con módulos ES y Firebase. **No abras el archivo con `file://`**; usá un servidor HTTP local:

```bash
cd /home/technoboy/Projects/gastos-viaje
python3 -m http.server 8080
```

Abrí en el navegador: [http://localhost:8080/gastos-viaje.html](http://localhost:8080/gastos-viaje.html)

Alternativa con Node:

```bash
npx --yes serve -l 8080
```

### Login y sincronización

- En la pantalla de login, usuario `**magus**` (definido en el script como `AUTH_LOGIN`).
- La contraseña es la que configuraste en Firebase Authentication para el correo `magus@gastos-brasil.app`.
- Los datos se guardan en Firestore (`viaje/datos`). Sin sesión no se cargan ni guardan gastos.

### Pruebas rápidas en consola

Abrí la app con `?selftest` en la URL para ejecutar aserciones de agregación por mes (consola del navegador):

`http://localhost:8080/gastos-viaje.html?selftest`