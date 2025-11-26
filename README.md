# Instruktion för att utföra *blink* med Arduino IDE och Pulsivo 

Detta repo redogör hur man genom Arduino IDE och Plusivo kan utför "blink" funktionen på NodeMCU microcontroller.

## Förutsättningar 
För att kunna utföra detta behöver du följande:
* ladda ner mjukvaroprogrammet Arduino IDE till din dator och ett Pulsivo kit med en NodeMCU microcontroller, dessa ser ut på följande sätt:
<p>
  <img src="arduino.png" width="300">
  <img src="arduinologo.png" width="150">
  <img src="IMG_2828.jpg" width="200">
  <img src="IMG_2829.jpg" width="200">
</p>

## Förbederelser Arduino och Pulsivo
När Arduino IDE är nedladdat behöver du göra följande:

1. Öppna programmet och `klicka`på progammtiteln i vänstra hörnet, därefter gå till *preferences* och klistra in följande URL-kod: `https://arduino.esp8266.com/stable/package_esp8266com_index.json`
2. Gå till *borads manager* och skriva in `esp8266`och installera ( de kan ta tid, var tålmodig)
3. Gå in på *Tools* -> *board* och tyck på *esp8266* -> välja versionen högst upp som heter `Generic ESP8266 Module`

Öppna ditt Pulsivo kit och se till att du har följande:
* NODEMCU (microcontroller)
* Breadborad (för att fästa microcontrollen på) 
* USB/ USB-C cable - Type A. Beroende på vilken dator du har behöver du viss kabel, en Mac behöver en USB-C och en Windows behöver en USB. 
   
## Testa *blink* funktion

1. Öppna upp Arduino IDE och gå till *File* -> *exampels* -> *01 basic* och välj *blink*
2. Ett nytt fönster kommer öppna, det är där du vill vara.
3. Fäst micro controllerns pinnar/ben i *breadbordet* 
4. Koppla in Type A kablen i microcontroller där de finns en port och USB (C) delen i din dator.
5. På Arduino gå in på *Tools* -> *Port* och välj Microcontrollern
6. Klicka på *veryfi* och sedan *upload* (detta kan ta en stund) Nu kommer microcontrollern börja blinka!
7. Scrolla ner till rad 32 - 36 är. Denna kod för att justera hur microconotllern blinkar och är som de står i en loop, vilket innebär att när programmet körs kommer samma procedur uppståom och om igen.
9. Rad 34 och 36 heter *delay* och följs av siffor - detta innebär hur lång tid de ska gå mellan att lappan lyser och sedan slocknar. Detta där förinställt på en tusendels sekund.
10. Denna tid kan man ändra genom att exempelvis ta bort en nolla, eller fler. Exmeplvis testade jag att ta bort alla nollor, detta gör att lampan lyser konstant istället för att blinka.

kom ihåg att så fort du ändrar något behöver du tycka på verify och upload!










