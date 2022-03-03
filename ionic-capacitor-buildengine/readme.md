# Docker Image to build iOS and Android Apps based on Capacitor

With this Image, and the corresponding compose file you can simply build you app regardless of the dev environment on the host system. 

`docker-compose up -d`
and 
`docker-compose exec ionic-builder sh`

With does 2 commands you are inside the project and can run any ionic command you are used to.

## iOS Build 

The ios build command `ionic capacitor build ios` can produce an error at the end.
Like: `[capacitor] /bin/sh: 1: xcodebuild: not found`

To verify the correct installation you can execute: `pod install --project-directory=ios/App` if this command succeeds you are set, and you can start xcode on your host to build the app.