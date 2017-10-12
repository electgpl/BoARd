# Board

Placa de desarrollo basada en Microchip de bajo costo, proyecto realizado de manera simple para poder ser replicado por alumnos de escuelas sin la necesidad de importar componentes y con la facilidad de realizar el circuito impreso por ellos mismos en una sola capa

  - [picc] PIC16F883 con Bootloader (Carga de fuente y Terminal Serie)
  - PCB Simple en 1 Layer realizado con Eagle
  - Bootloader oficial Micochip (AN1310)
  - Multiples IDEs y lenguajes

Se ha probado con diversos IDEs y Lenguajes con resultados satisfactorios

> [picc] - PCWHD (PICC)
> [mplabx] - MPALB X
> [mikroc] - MikroC
> [ldmicro] - LDmicro
> [eagle] - Eagle

## Lenguajes

* Assembly
* C
* C++
* Basic
* Visual
* Ladder
* Scratch

### Instalacion (Windows)

Dillinger requires [Node.js](https://nodejs.org/) v4+ to run.

Install the dependencies and devDependencies and start the server.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

For production environments...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Plugins

Dillinger is currently extended with the following plugins. Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md] [PlDb] |
| Github | [plugins/github/README.md] [PlGh] |
| Google Drive | [plugins/googledrive/README.md] [PlGd] |
| OneDrive | [plugins/onedrive/README.md] [PlOd] |
| Medium | [plugins/medium/README.md] [PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md] [PlGa] |


### Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantanously see your updates!

Open your favorite Terminal and run these commands.

First Tab:
```sh
$ node app
```

Second Tab:
```sh
$ gulp watch
```

(optional) Third:
```sh
$ karma test
```
#### Building for source
For production release:
```sh
$ gulp build --prod
```
Generating pre-built zip archives for distribution:
```sh
$ gulp build dist --prod
```
### Docker
Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the Dockerfile if necessary. When ready, simply use the Dockerfile to build the image.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version}
```
This will create the dillinger image and pull in the necessary dependencies. Be sure to swap out `${package.json.version}` with the actual version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on your host. In this example, we simply map port 8000 of the host to port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

See [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)


### Todos

 - Write MORE Tests
 - Add Night Mode

License
----

MIT


**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [picc]: <http://www.ccsinfo.com/>
   [mplabx]: <http://www.microchip.com/mplab/mplab-x-ide>
   [eagle]: <https://www.autodesk.com/education/free-software/eagle>
   [mikroc]: <https://www.mikroe.com/mikroc/>
   [ldmicro]: <http://cq.cx/ladder.pl>

