# Arduino_Calling_Dallas_MultiBus
DS18B20 sensors split onto multiple buses to reduce individual bus weight. Max buses 10, max sensors per bus 10.

Previous attempts were retrieving the data directly from the onewire bus. This lead to 0s being stripped from the serial number causing varaiblility in string length. Sensors would start disappearing/reappearing randomly. when adding the 15th sensor. Suspected hardware limitation. (non genuine sensros, different cable types, combinng star and spur topology, non genuine arduino uno).
Have now confirmed parasitic power isnt being used, changed wiring config which requres seperate resisitor per bus. using 2.15kohms.

