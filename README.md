 
 #  angular-pushNotifications

Implementation of angular push notification as per angular docs

## Installation

Run on terminal

```bash
ng add @angular/pwa --project *project-name*
```
This will add following files : @angular/service-worker package,manifest.webmanifest ,ngsw-config.json

In app.module.ts add 

```bash
ServiceWorkerModule.register('/ngsw-worker.js', { enabled: environment.production})
```
Make a build using
```bash
ng build --prod
```

Now install a http server,as ng serve does not work with service workers, you must use a separate HTTP server to test your project locally
Make a build using
```bash
npm i http-server
http-server -p 8080 -c-1 dist/(folder name if any that contains build)
```
Open http://localhost:8080 ,you can see your application working
Now turn off network from 
    ```bash inspect->networks tab->online to offline ```
Reload page,it will still work

##
  **This means that the resources are not being loaded from the network. Instead, they are being loaded from the service worker's cache.**

    
