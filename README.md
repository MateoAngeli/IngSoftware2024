# Laboratorio Ing. Software I (2024, FAMAF)

This is a group project developed using agile methodologies.

# frontend
Repositorio utilizado para desarrollar el frontend del laboratorio

# Proyecto React con Vite

Este proyecto está creado utilizando **Vite** para el desarrollo de una aplicación en **React**.

## Requisitos previos

Antes de comenzar, asegúrate de tener instalado lo siguiente en tu sistema:

- [Node.js](https://nodejs.org) (versión 14 o superior)
- npm (que se instala junto con Node.js)

Puedes verificar que tienes Node.js y npm ejecutando los siguientes comandos en tu terminal:
```bash
node -v
npm -v
```

## Crear un nuevo proyecto

Sigue estos pasos para iniciar un proyecto de React con Vite:

1. **Crear el proyecto**:

   Ejecuta el siguiente comando en tu terminal para crear un nuevo proyecto con Vite:
   ```bash
   npm create vite@latest nombre-del-proyecto
   ```

2. **Selecciona React**:

   Cuando se te pida elegir un framework, selecciona **React**. También puedes optar por JavaScript o TypeScript según tus necesidades.

3. **Instala las dependencias**:

   Ingresa al directorio del proyecto y ejecuta el siguiente comando para instalar todas las dependencias necesarias:
   ```bash
   cd nombre-del-proyecto
   npm install
   ```

## Ejecutar el servidor de desarrollo

Una vez instaladas las dependencias, puedes iniciar el servidor de desarrollo ejecutando el siguiente comando:
```bash
npm run dev
```

Esto abrirá tu aplicación en el navegador en la URL [http://localhost:5173](http://localhost:5173). Cualquier cambio que realices en el código se reflejará automáticamente gracias a Vite.

## Crear una versión de producción

Cuando estés listo para crear una versión de producción optimizada, ejecuta:
```bash
npm run build
```

Esto generará una carpeta `dist` que contendrá todos los archivos listos para desplegar.

## Scripts disponibles

Además de los comandos mencionados anteriormente, aquí tienes algunos scripts adicionales disponibles en el proyecto:

- **`npm run dev`**: Inicia el servidor de desarrollo.
- **`npm run build`**: Crea una versión de producción optimizada.
- **`npm run preview`**: Previsualiza localmente la versión de producción generada por `build`.

## Estructura del proyecto

- **`src/`**: Contiene todos los archivos de código fuente de React.
- **`public/`**: Archivos públicos que no requieren procesamiento (como imágenes o `index.html`).
- **`vite.config.js`**: Configuración de Vite.
- **`node_modules/`**: Dependencias instaladas por npm.

## Más información

Para obtener más información sobre cómo usar Vite, visita la [documentación oficial de Vite](https://vitejs.dev).



# Backend
Repositorio utilizado para desarrollar el backend del laboratorio

## Requisitos previos

Antes de comenzar, asegúrate de estar en un entorno virtual.
Puedes utilizar el siguiente.
- [venv](https://docs.python.org/es/3/library/venv.html)

Crear entorno virtual:
```bash
python3 -m venv .venv
```

Activa tu entorno virtual:
```bash
source .venv/bin/activate
```
una vez activado el entorno virtual puedes verificar que estan en uno con el siguiente comando
```bash
which python
/home/user/code/awesome-project/.venv/bin/python
```
para salir del entorno virtual utiliza 
```bash
deactivate
```
## Dependencias del proyecto

Ejecuta los siguientes comandos para instalar las dependencias del proyecto:

```bash
pip install fastapi==0.108.0
pip install uvicorn
pip install 'uvicorn[standard]'
```

```bash
pip install SQLalchemy
```

Asegúrate de que el directorio src esté en el PYTHONPATH para que los módulos puedan ser encontrados correctamente. Puedes hacerlo temporalmente en tu terminal antes de ejecutar pytest:

```bash
export PYTHONPATH=$PYTHONPATH:/tu/ruta/al/proyecto/backend/src
```

y para ejecutar nuestro servidor iremos al path de nuestro archivo a corre y ejecutaremos el comando

```bash
uvicorn app:app --reload
```

Ahora para ver la documentacion del mismo con ir a la pagina
*http://127.0.0.1:8000/docs* podremos ver todos los endpoints de nuestra api.

## Runear los test

Primero hay que descargar las dependencias.

```bash
pip install httpx
pip install pytest-asyncio
pip install pytest
pip install coverage
pip install factory_boy
```

Hay que estar en la dirección `/backend/src` y ahí se ejecuta el comando:

```bash
coverage run -m pytest -v
```

Despues para ver el respuen del test se ejecuta:

```bash
coverage report -m
```

## Organizacion de archivos

**`src/`**: Carpeta principal para el código fuente.

**`models/`**: Contiene las clases y sus metodos.

**`routes/`**: Contiene todos los endpoints de cada clase.

**`test/`** Contiene todos los test.

**`app.py`** Contiene el manejo principal de la API.
