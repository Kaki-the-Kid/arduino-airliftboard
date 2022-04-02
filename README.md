# Arduino airlift board

Airlift fra Adafruit er et shield som giver en Arduine Uno mulighed for at komme på internettet 

Det fulde navn på shield er:
Adafruit AirLift Shield - ESP32 WiFi Co-Processor

AdaFruit dokumentation:
Produkt side: https://www.adafruit.com/product/4285


Primary Guide: Adafruit AirLift Shield - ESP32 WiFi Co-Processor
Add an AirLift Shield to give your projects an internet or BLE-enabled lift!

https://learn.adafruit.com/adafruit-airlift-shield-esp32-wifi-co-processor


# Beskrivelse af shield
BESKRIVELSE
Giv dit Arduino-projekt et løft med Adafruit AirLift Shield - et skjold, der lader dig bruge den kraftfulde ESP32 som en WiFi-co-processor. Du har sikkert din favorit Arduino-kompatible (som Metro M4 eller den klassiske Metro 328), der kommer med sit eget sæt fantastiske perifere enheder og masser af biblioteker. Men den har ikke WiFi indbygget! Så lad os give den chip en bedste ven, ESP32. Denne chip kan håndtere alle de tunge løft ved at oprette forbindelse til et WiFi-netværk og overføre data fra et websted, selvom den bruger den nyeste TLS/SSL-kryptering (den har rodcertifikater forudbrændt).

At have WiFi administreret af en separat chip betyder, at din kode er enklere, du behøver ikke at cache socket-data eller kompilere og debugge et SSL-bibliotek. Send grundlæggende, men kraftfulde socket-baserede kommandoer over 8MHz SPI til højhastigheds dataoverførsel. Du kan bruge en hvilken som helst 3V eller 5V Arduino, enhver chip fra ATmega328 eller op (selvom '328 ikke vil være i stand til at udføre meget komplekse opgaver eller buffere en masse data). Det fungerer også godt med CircuitPython, et SAMD51/Cortex M4 minimum påkrævet, da vi har brug for en masse RAM. Alt du behøver er SPI-bussen og 2 kontrolben plus en strømforsyning, der kan levere op til 250mA under WiFi-brug.

Vi placerede et ESP32-modul på et skjold med en separat 3,3V regulator og en tri-state chip til MOSI, så du kan dele SPI-bussen med andre skjolde. Vi har også smidt et micro SD-kortstik, du kan bruge det til at hoste eller gemme data, du får fra internettet. Arduino'er baseret på ATmega328 (ligesom UNO) kan ikke bruge både WiFi-modulet og SD-biblioteket på samme tid, de har ikke nok RAM. Igen anbefaler vi et M0- eller M4-chipsæt til brug med Arduino, M4 til CircuitPython!

Kommer fuldt samlet og testet, forprogrammeret med ESP32 SPI WiFi co-processor firmware, som du kan bruge i CircuitPython til at bruge denne til WiFi co-processor. Vi inkluderer også noget header, så du kan lodde det ind og tilslutte det direkte til din Arduino-kompatible, men du kan også hente et sæt stable headers til at stable over/under dit board.

Vi har testet dette med alle vores metroer, og det burde fungere fint med dem undtagen Metro M4 Airlifts (fordi de allerede har WiFi!). Til brug i Arduino, '328 og '32u4 kan du lave grundlæggende tilslutningsmuligheder og dataoverførsel, men de har ikke meget RAM, så vi anbefaler dem ikke - brug Metro M0, M4 eller lignende, for de bedste resultater! Til CircuitPython-brug fungerer en Metro M4 bedst - M0-serien har ikke nok RAM i CircuitPython.

Firmwaren ombord er en lille variant af Arduino WiFiNINA kernen, som fungerer fantastisk! På nuværende tidspunkt er forbindelse til Enterprise WiFi ikke understøttet endnu.

# Videre læsning
* Github - adafruit / Adafruit_CircuitPython_ESP32SPI<br />https://github.com/adafruit/Adafruit_CircuitPython_ESP32SPI
* Adafruit AirLift Shield - ESP32 WiFi Co-Processor<br />https://learn.adafruit.com/adafruit-airlift-shield-esp32-wifi-co-processor