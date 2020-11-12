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