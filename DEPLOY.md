# SS Streetwear — publicación en .COM

## 1. Subir a GitHub
Sube todo el contenido de este proyecto a un repositorio nuevo.

## 2. Crear el servicio
En Render crea un Web Service conectado al repositorio.

- Build Command: `pip install -r requirements.txt`
- Start Command: `gunicorn backend.app:app`

## 3. Variables de entorno
Configura:
- `SECRET_KEY` = una cadena secreta larga (Render puede generarla)
- `ADMIN_PASSWORD` = tu contraseña de administrador
- `SITE_URL` = `https://TU-DOMINIO.com`

## 4. Dominio .COM
Compra tu dominio con el registrador que prefieras y agrega en su DNS los registros que Render indique para tu dominio personalizado.

## 5. Comprobación
Después de desplegar:
- `https://TU-DOMINIO.com/`
- `https://TU-DOMINIO.com/health`

La segunda dirección debe responder con `{"status":"ok"}`.

## Nota sobre SQLite
Este proyecto usa SQLite. En un hosting con almacenamiento efímero, la base de datos puede perderse al redeploy. Para una tienda real conviene migrar a PostgreSQL antes de manejar muchos pedidos.
