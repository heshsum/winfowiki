# Setup
## Woher bekomme ich Java?
Um mit Java zu programmieren (bzw. zu kompilieren) oder Java-Programme auszuführen benötigt man Java, denn Java wird nicht direkt zu Maschinencode kompiliert, sondern es wird Code für die Java Virtual Machine (JVM) gebaut.  
Der Vorteil ist, dass dasselbe Programm auf viele Plattform lauffähig ist.  
Der Nachteil liegt darin, dass die Maschine eine solche JVM zur Verfügung stellen muss (sprich: Java muss installiert sein).

Für das bloße Ausführen reicht das Java Runtime Environment (JRE). Um damit zu entwickeln benötigt man das Java Development Kit.  

Als freies JDK ist das [Adoptium JDK](https://adoptium.net) empfehlenswert.

## Welche Java-Version habe ich?
Am einfachsten fragt man einfach Java selbst:
```bash
java --version
```

Die Antwort könnte in etwa so aussehen:
```bash
> java --version
openjdk 19.0.1 2022-10-18
OpenJDK Runtime Environment Temurin-19.0.1+10 (build 19.0.1+10)
OpenJDK 64-Bit Server VM Temurin-19.0.1+10 (build 19.0.1+10, mixed mode)
```

## Welcher Editor?
Zwar kann man Java mit einem beliebigen Editor programmieren, aber es empfiehlt sich die Nutzung einer IDE. IDEs wie [Eclipse](https://www.eclipse.org/) oder [IntelliJ](https://www.jetbrains.com/de-de/idea/) machen die Programmierung sehr viel leichter und angenehmer. Auch [Visual Studio Code](https://code.visualstudio.com) ist als Java Editor nicht verkehrt.