# Configureren linux
Gebruik je je eigen laptop tijdens het practicum zorg dan dat je eerst git en een Java Development Kit (JDK) hebt geïnstalleerd en dat de Java Runtime Environment (JRE) en de JDK dezelfde versie zijn. De stappen daarvoor zijn hieronder beschreven. We gaan uit van Ubuntu 12.10.

## Installeren

Open een terminal en voer het volgende commando uit om git te installeren:

    sudo apt-get install git

In de meeste gevallen staat er al een JRE geïnstalleerd. Zorg dan dat je een JDK installeerd van dezelfde versie. Je kan als volgt de JRE versie controleren:

    java -version
    
Je krijgt hieruit waarschijnlijk versie 1.7.* of 1.6.*. Om te kijken of er ook een JDK geïnstalleerd staat kan je het volgende commando uitvoeren. Als deze dezelfde versie hebben is alles in orde en hoef je de rest van deze handleiding niet te volgen.

    javac -version

Als je nog geen JDK hebt en je JRE is versie 1.6.* voer dan het volgende uit:

    sudo apt-get install openjdk-6-jdk

En voor versie 1.7.*:

    sudo apt-get install openjdk-7-jdk

## Configureren

Zijn je JRE en JDK niet dezelfde versie dan moet je de goede versie installeren en Ubuntu instrueren de juiste versie te gebruiken. Gebruik de volgende commando's om de gebruikte versie van respectievelijk de JRE en JDK te kiezen.

    sudo update-alternatives --config java
    sudo update-alternatives --config javac
