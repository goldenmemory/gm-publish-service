# gm-publish-service

1. git clone git@github.com:goldenmemory/gm-publish-service.git

2. cd gm-publish-service/initial/

3. ./gradlew build buildDocker

4. docker run -p 443:443 -t 1form/gm-publish-service

5. open https://api.local.gm.chatops.in/greeting in browser

6. open the project in IntelliJ

7. Run -> Edit Configurations, "+" -> application, 
Main class = "org.springframework.boot.devtools.RemoteSpringApplication"
Program arguments = "https://api.local.gm.chatops.in"
User classpath of module = "gm-publish-service_main"

Command + , -> Build, Execution, Deployment -> Compiler -> Check "Make project automatically"
Apply & Ok
 
8. Use firefox to download the certificate

9. keytool -import -alias api.local.gm -keystore /Library/Java/JavaVirtualMachines/jdk1.8.0_73.jdk/Contents/Home/jre/lib/security/cacerts -file [the path of certificate you've just downloaded]

Enter ketstore password: changeit

10 .  
1 - Enable Automake from the compiler

PRESS: CTRL + SHIFT + A
TYPE: make project automatically
PRESS: Enter
Enable Make Project automatically feature
2 - Enable Automake when the application is running

PRESS: CTRL + SHIFT + A
TYPE: Registry
Find the key compiler.automake.allow.when.app.running and enable it


11. Run application
