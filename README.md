# gm-publish-service

## Config your local env and IntelliJ IDE

1. `git clone git@github.com:goldenmemory/gm-publish-service.git`

2. `cd gm-publish-service/`

3. `./gradlew build buildDocker`

4. `docker run -p 443:443 -t 1form/gm-publish-service`

     ```open https://api.local.gm.chatops.in/greeting in browser to check.```

5. open the project in IntelliJ

6. Run -> Edit Configurations -> "+" -> application,
   Main class = "org.springframework.boot.devtools.RemoteSpringApplication"
   Program arguments = "https://api.local.gm.chatops.in"
   User classpath of module = "gm-publish-service_main"

7. Command + , -> Build, Execution, Deployment -> Compiler -> Check "Make project automatically"
 
8. Use firefox to download the certificate

9. keytool -import -alias api.local.gm -keystore /Library/Java/JavaVirtualMachines/jdk1.8.0_73.jdk/Contents/Home/jre/lib/security/cacerts -file [the path of certificate you've just downloaded]

   Enter ketstore password: changeit

10. Enable Automake when the application is running

   PRESS: CTRL + SHIFT + A
   TYPE: Registry
   Find the key compiler.automake.allow.when.app.running and enable it

11. Run application
