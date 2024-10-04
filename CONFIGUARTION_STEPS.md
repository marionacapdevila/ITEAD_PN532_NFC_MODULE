# ITEAD_PN532_NFC_MODULE

Steps:

1. Preparem la targeta SD
Primer descarreguem Raspberry Pi Imaginer i connectem la targeta SD al lector SD, i aquest al nostre ordinador.

Obrim l'aplicació Raspberry Pi Imager per gravar el sistema operatiu a la targeta. Escollirem el sistema operatiu Raspberry Pi OS (64-bit), el model de la nostra placa i seleccionarem la nostra targeta microSD.

Abans de continuar, editarem la configuració per habilitar el SSH per poder connectar-nos remotament i configurarem un usuari i una contrasenya que haurem de recordar. Ara també podem escollir si connectar-nos a la nostra Raspberrry a través del WiFi o Ethernet, com que jo ho faré amb Ethernet, deixem la configuració del WiFi en blanc.

Finalment, ja podem escriure la imatge a la targeta SD i, un cop acabi, la introduirem a la nostra Raspberry Pi.

2. Trobar la IP de la nostra Raspberry Pi

Obrim les 'Connexions de xarxa' al nostre portàtil. Allà, entrarem a 'Ethernet' per buscar la IP que li correspon. En el meu cas és: 192.168.137.1.

Ara obrirem l'aplicació 'Advanced IP Scanner', introduirem la IP trobada aplicant la màscara /24. D'aquesta manera farem un sondeig precís per trobar la IP de la nostra Raspberry Pi. En el meu cas és: 192.168.137.249.

3. Connectar-nos a la Raspberry

Obrirem PuTTY on configurarem el següent: al Host Name escriurem raspberrypi.local, marcarem que la connexió es farà amb SSH, guardarem la sessió amb un nom (en el meu cas raspberry_ethernet) i clicarem open. Dins haurem de posar l'usuari i contrasenya configurats al SD. Un cop fet això, escriurem 'sudo raspi-config' per accedir a 'interface options' i activar la sincronització amb el nostre visualitzador clicant VNC, ara ja està preparada per rebre connexions VNC.

L'aplicació 'RealVNC Viewer' és la que utilitzem com a visualitzador, per poder utilitzar-lo com a monitor. Dins, a adress, posarem la IP de la nostra Raspberry i aquest ens obrirà una pantalla, ja estem dins.
