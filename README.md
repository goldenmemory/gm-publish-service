# gm-publish-service

## Config your local env and IntelliJ IDE

### `git clone git@github.com:goldenmemory/gm-publish-service.git`

### `cd gm-publish-service/`

### `./gradlew build buildDocker`

### `docker run -p 443:443 -t 1form/gm-publish-service`

     ```open https://api.local.gm.chatops.in/greeting in browser to check.```

### open the project in IntelliJ

### Run -> Edit Configurations -> "+" -> application,
    Main class = "org.springframework.boot.devtools.RemoteSpringApplication"
    Program arguments = "https://api.local.gm.chatops.in"
    User classpath of module = "gm-publish-service_main"

### Command + , -> Build, Execution, Deployment -> Compiler -> Check "Make project automatically"
 
### Use firefox to download the certificate

### keytool -import -alias api.local.gm -keystore /Library/Java/JavaVirtualMachines/jdk1.8.0_73.jdk/Contents/Home/jre/lib/security/cacerts -file [the path of certificate you've just downloaded]

    Enter ketstore password: changeit

### Enable Automake when the application is running

   PRESS: CTRL + SHIFT + A
   TYPE: Registry
   Find the key compiler.automake.allow.when.app.running and enable it

### Run application
