## Angular Progressive Web Apps Course Helicopter View:
- Two parts:
    1. Angular-specific.
    2. Service workers, including lifecycle.
	    - Chrome PWA Dev Tools.

## Course Kick-Off: Install Node, NPM, IDE And Service Workers Section Code:
- https://github.com/angular-university/angular-pwa-course
- package-lock.json ensures that the same dependencies are locked into place.
```javascript
    npm install
    npm audit fix
    npm run server
```
- proxy.json file intercepts API calls.
```javascript
    {
    "/api": {
        "target": "http://localhost:9000",
        "secure": false
    }
    }
```
```javascript
    npm start
```

## How To Convert an Angular Application Into a PWA
```javascript
    npm install --save @angular/service-worker
```
- Modify configuration:
```javascript
    "buildOptimizer": true,
    "serviceWorker": true,
    "ngswConfigPath": "src/ngsw-config.json",
    "fileReplacements": [
```
- This is a build step configuration file. So we'll test it:
```javascript
    ng build
```

## How To Run The Angular Service Worker In Production Mode:
- We'll run the production application after installing a small http server.
```javascript
    cd dist
    npm install -g http-server
```
- Note: disable caching headers: -c-1
- Always proxy requests: -P http://localhost:9000
```javascript
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    http-server -c-1 -P http://localhost:9000 .
```

## Angular Service Worker - How Does it Work: