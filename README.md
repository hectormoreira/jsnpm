# Curso de Gestión de Dependencias y Paquetes con NPM

Notas del [Curso de Gestión de Dependencias y Paquetes con NPM](https://platzi.com/clases/npm/)

## Iniciar proyecto
```sh
mkdir jsnpm
cd jsnpm
git init
init npm

```

**Otras vías**, se puede crear valores por defecto:
```sh
npm set init.author.email "email@gmail.com"
npm set init.author.name "mi_nombre"
npm set init.license "MIT"
npm init -y
```

## Conceptos
- Dependencias desarrollo con el flag --save-dev
- shortcut flag i es install
- -g para instalar dependencias flobales
- `npm list -g --depth 0` ver dependencias globales
- `--dry-run` simula instalación y retorna el output
- `-f` fuerza la instalacion desde los servidores de npm
- `npm install` instalada todas las dependencias registradas en `package.json`
- Revisar que paquetes disponen de nuevas versiones `npm outdate`
- Para ver un output más detallado `npm outdate --dd`
- Actualizar los paquetes que no están en la ultima versión `npm update`
- Actualizar un paquete especifico `npm install json-server@latest`
- Eliminar un paquete de node_modules y del archivo `package.json` `npm uninstall json-server`
- Desinstalar un paquete de todo node_modules pero no del archivo `package.json` `npm uninstall webpack --no-save`
- **Versionado**  (ej version 3.9.2 )
    - **Major**: Cambio mayor
    - **Minor**: Cambios menores, se agrega funcionalidades menores
    - **Patch**: Parches, bug fix
    - ^ = Si mantenemos el caret dentro de la configuración de nuestro package estamos garantizando que cuando realicemos una actualización o tengamos un cambio que podamos realizar, vamos a hacer actualización de los cambios menores y de los parches o bug fixes.
    - Para quedarnos en una sola versión eliminamos el caret
        - ~ = Establece que vamos a recibir actualizaciones o cambios solamente de los cambios que son parches o bug fixes.
- Commando por defecto `npm test` ejecuta los test registrados.
- **Solución de problemas**
    - Activar la opción de verbose (es decir que nos muestre mayor información de lo que esta haciendo el comando) `npm run [comando] --dd`
    - `npm cache clear --force` Limpiar caché
    - `npm cache verify` verificar borrado
    - `rm -rf node_modules` eliminar carpeta
    - `sudo npm install -g rimraf` alternativa para eliminar de forma segura una carpeta es instalando el siguiente paquete
    - `rimraf node_modules` eliminar usando rimraf
- **Seguridad**
    - `npm audit` auditar nuestro proyecto
    - `npm audit --json` información detallada del audit en json
    - `npm update [paquete] --depth 2` actualizar paquetes con vulnerabilidades
    - `npm audit fix` solucionar vulnerabilidades
    - snyk.io es una herramienta que busca vulnerabilidades

- `npm link` se instala (referencia) nuestro paquete a nivel global como si lo hicieramos desde npm
- `npm install -g [path]` Otra vía para instalar nuestro paquete en local 
- `npm adduser` registrar en npm vía cmd
- `npm publish` publicar en npm
- `npm version patch` solo parches
- `npm version minor` cambios menores
- `npm version major` cambios mayores
- `npm install -g npm` actualizar npm



### Dependencias
```sh
npm install moment --save-dev
npm i date-fns -D
npm i -g nodemon
npm install eslint -O
npm install webpack -f
```

## Proyecto del curso
```sh
pwd
mkdir random-messages
cd random-messages
npm init
```