# PIB-PA: Einführung in die Demoszene

## Deutsch
## Beschreibung
Dieses Repository beinhaltet nur die Demo sowie den Sourcecode selbst innerhalb des Verzeichnisses "Demo-Code".

Diese Software ist als Teil einer Projektarbeit im Rahmen des Kurses PIB-PA der htw saar zusammen mit dem Nutzer Inkzxd entwickelt worden.
Sie beinhaltet eine selbst entwickelte Demo, die sich im Bereich der Demoszene bewegt.
Innerhalb der Demo wird ein Retro-Terminal sowie der Start einer Datei innerhalb dieses Terminals simuliert.
Die Demo besteht dabei aus den folgenden Komponenten:
- Ein Login-Screen, der die Authentifizierung eines Benutzers simuliert.
- Ein Terminal-Screen, der den Start von C++-Code innerhalb des Retro-Terminals simuliert.
- Eine Karten-Sequenz, in der die Ortung verschiedener vorgegebener Koordinaten simuliert wird.
Unterbrochen wird dieser Szenen-Ablauf durch den Kollaps und Wiederaufbau des Bildschirms. Dies passiert sowohl zwischen dem
Terminal-Screen und der Karten-Sequenz als auch nach Ablauf der Karten-Sequenz, worauf ein erneuter Durchgang der Demo folgt.

## Benötigte Software
Zum Ausführen dieser Demo wird Visual C++ 2013 Redistributable benötigt.
Dies kann unter https://www.microsoft.com/en-us/download/details.aspx?id=40784 heruntergeladen werden.
Dabei müssen die x86- und x64-Versionen installiert werden.

## Config-Datei
Die Demo beinhaltet eine Config-Datei, mit der die Bildschirmauflösung und Vollbildmodus konfiguriert werden können. Die Datei hat das folgende Format:

```ini
[Window]
Width=1920
Height=1080
Fullscreen=false
```

Die Werte können nach Bedarf angepasst werden. Das Programm muss dazu nicht neu kompiliert werden. Die Datei befindet sich im selben Verzeichnis wie die start.bat.

## Kompilieranleitung
Die Demo kommt standardmäßig mit einer kompilierten Version der Anwendung. 
Zur Kompilierung der Demo wird die MSYS2 MinGW64-Umgebung benötigt. Die folgenden Schritte sind erforderlich:
1.  Installieren Sie MSYS2 von https://www.msys2.org/
2.  Öffnen Sie die MSYS2 MinGW64-Shell.
3.  Aktualisieren Sie die Paketdatenbank und installieren Sie die benötigten Pakete:´
    - pacman -Syu (Aktualisierung der Paketdatenbank)
    - pacman -S --needed mingw-w64-x86_64-toolchain
    - pacman -S mingw-w64-x86_64-cmake
    - pacman -S mingw-w64-x86_64-glfw
    - pacman -S mingw-w64-x86_64-freetype
    - pacman -S mingw-w64-x86_64-glm
    - pacman -S mingw-w64-x86_64-sfml
4. Klonen Sie das Repository und wechseln Sie in das Verzeichnis "pa_demoszene"
5. Kompilierung des Projekts:
    - mkdir build
    - cd build
    - cmake -G "MinGW Makefiles" ..
    - mingw32-make
6. Wechseln Sie zurück in das Oberverzeichnis durch "cd .."
7. Nach der Kompilierung finden Sie die ausführbare Datei im Verzeichnis "pa_demoszene".
8. Starten der Anwendung entweder durch Ausführen der beiliegenden start.bat oder durch Eingabe des Befehls ./RetroTerminal in der MinGW64-Shell.


## English
## Description
This repository only contains the demo and the source code itself within the directory "Demo-Code".

This software was developed as part of a project for the PIB-PA course at htw saar together with the user Inkzxd.
It includes a self-developed demo as part of the demo scene.
The demo simulates a retro terminal and the launch of a file within this terminal.
The demo consists of the following components:
- A login screen that simulates user authentication.
- A terminal screen that simulates the launch of C++ code within the retro terminal.
- A map sequence that simulates the location of various specified coordinates.
This sequence of scenes is interrupted by the collapse and reconstruction of the screen. This happens both between the
terminal screen and the map sequence and after the map sequence has ended, followed by another run of the demo.

## Software requirements
Visual C++ 2013 Redistributable is required to run this demo.
It can be downloaded at https://www.microsoft.com/en-us/download/details.aspx?id=40784.
Both the x86 and x64 versions must be installed.

## Config file
The demo includes a config file that can be used to configure the window size and fullscreen mode.
The file has the following format:

```ini
[Window]
Width=1920
Height=1080
Fullscreen=false
```

The values can be adjusted as needed. The program does not need to be recompiled. The file is located in the same directory as the start.bat.

## Compiling the demo
The demo comes with a pre-compiled version of the application.
To compile the demo, the MSYS2 MinGW64 environment is required. The following steps are required:
1. Install MSYS2 from https://www.msys2.org/
2. Open the MSYS2 MinGW64 shell.
3. Update the package database and install the required packages:
    - pacman -Syu (Update the package database)
    - pacman -S --needed mingw-w64-x86_64-toolchain
    - pacman -S mingw-w64-x86_64-cmake
    - pacman -S mingw-w64-x86_64-glfw
    - pacman -S mingw-w64-x86_64-freetype
    - pacman -S mingw-w64-x86_64-glm
    - pacman -S mingw-w64-x86_64-sfml
4. Clone the repository and change to the "pa_demoszene" directory.
5. Compile the project:
    - mkdir build
    - cd build
    - cmake -G "MinGW Makefiles" ..
    - mingw32-make
6. Change back to the parent directory through "cd .."
7. After compilation, the executable file can be found in the "pa_demoszene" directory.
8. Start the application either by running the attached start.bat or by typing the command ./RetroTerminal in the MinGW64 shell.
