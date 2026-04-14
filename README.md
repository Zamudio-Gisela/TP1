# ARCHIVO .gitignore

## Porque es conveniente incluirlo?

Sirve para especificar cuales son los archivos o carpetas que no deben ser rastreados,
controlados ni subidos al repositorio. Su proposito principal es mantener el proyecto 
limpiio, excluir los archivos generados automaticamente, evitar confilctos de configuracion
local y proteger datos sensibles, como llaves API o contraseñas.

Aspectos claves del archivo _.gitignore_:

- Evita el seguimiento de archivos
- Seguridad
- Limpieza del repositorio
- Ubicacion
- Funcionamiento

## Cuando se debe hacer?

_.gitignore_ solo funciona para archivos que aun no han sido rastreados (committed) por Git,
por lo que es conveniente y recomendable crear dicho archivo al inicio, antes de cualquier 
sincronizacion.

## Como configurar el archivo _.gitignore_?

El archivo _.gitignore_ es un archivo de texto colocado en el directorio raiz de tu repositorio
Git. Contiene patrones quie indican a Git cuales archivos o directorios debe ignorar. Estos 
patrones pueden personalizarse para adaptarse a las necesidades de tu proyecto, ayudandote a 
mantner un repositorio bien organizado.

**1. Construye artefactos:** Archivos generados durante el proceso de construccion que pueden 
volver a crearse a partir del codigo fuente, como:
- dist/ , build/ (salidas de contruccion fontend y backend)
- target/ (Java y otros lenguajes compilados)

**2. Dependencias:** Los sistemas de gestion de paquetes crean directorios para las bibliotecas 
instaladas, que no deben rastrearse:
- node_modules/ (Node.js)
- vendor/ (PHP, Compositor)
- .venv/ , venv/ (Entornos virtuales Python)

**3. Archivos especificos del sistema:** Estos archivos los genera automaticamente el sistema
operativo y no contribuyen al proyecto:
- .DS_Store (macOS)
- Thumbs.db (Windows)

**4. Archivos de configuracion del IDE:** Cada desarrollador puede utilizar un entorno de desarrollo 
distinto, por lo  que su configuracion personal no debe incluirse en el control de versiones:
- .vscode/ (Codigo VS)
- .idea/ (IDEs JetBrains)
- .project , .settings/ (Eclipse)

**5. Registros y archivos temporales:** Los registros, caches y archivos temporales deben ignorarse
para evitar un desorden innecesario:
- npm-debug.log* , yarn-debug.log* , yarn-error.log* (Resgistros de varis herramientas)
- *.tmp , *.bak (Archivos temporales y de copia de seguridad)
- .mypy_cache/ , ___pycache/___ (caches de Python)
- .ipynb_checkpoints/ (Puntos de control de Jupiter Notebbok)

**6. Archivos de entorno y secretos:** Las credenciales sensibles y las configuraciones especificas 
del entorno nunca deben comprometerse:
- .env , .env.local , .env.development , .env.production
- secrets.json , config.json (Archivos de configuracion sensibles)

**7. Base de datos y archivos de almacenamiento:** Se generan localmente y no deben incluirse en el 
control de versiones:
- *.sqlite , *.sqlite3 , *.db (archivos de base de datos SQLite)
- dump.rdb (Volcado de la base de datos Redis)
 
**8. CI/CD y archivos de cobertura:** Los informes de cobertura de pruebas y otros artefactos de 
CI/CD deben ignorarse:
- coverage/ , *.lcov (Informes de cobertura de codigo)
- .tox/ , .pytest_cache/ (archivos de prueba de Python)

[gitignore.io] (https://www.toptal.com/developers/gitignore)
