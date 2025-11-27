# Instruktion för att utföra *blink* med Arduino IDE och Pulsivo 

I detta repo redogör jag för hur man genom Arduino IDE och Plusivo kan utför "blink" funktionen på en NodeMCU micro controller.

## Förutsättningar 
För att kunna utföra detta behöver du följande:
* ladda ner mjukvaroprogrammet Arduino IDE till din dator och ett Pulsivo kit med en NodeMCU micro controller, dessa ser ut på följande sätt:
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

När ovanstående är klart öppna ditt Pulsivo kit och se till att du har följande:
* NodeMCU (microcontroller)
* Breadborad (för att fästa micro controller på) 
* USB/ USB-C cable - Type A. Beroende på vilken dator du har behöver du viss kabel, en Mac behöver en USB-C och en Windows behöver en USB. 
   
## Testa *blink* funktion

1. Öppna upp Arduino IDE och gå till *File* -> *exampels* -> *01 basic* och välj *blink*
2. Ett nytt fönster kommer öppna, det är där du vill vara.
3. Fäst micro controllerns pinnar/ben i *breadbordet* 
4. Koppla in Type A kablen i micro controllern där de finns en port och USB (C) delen i din dator.
5. På Arduino gå in på *Tools* -> *Port* och välj Microcontrollern
6. Klicka på *veryfi* och sedan *upload* ikonerna -> <img width="90" height="50" alt="upload" src="https://github.com/user-attachments/assets/a24d6c8f-c823-4068-99c5-2889b44dd892" /> Nu kommer micro controllern börja blinka!
7. Scrolla ner till rad 32 - 36 är. Denna kod är för att justera hur NodeMCU blinkar och detta sker i en loop, vilket innebär att när programmet körs kommer samma procedur uppstå om och om igen.
8. Rad 34 och 36 heter *delay* och följs av siffor - detta innebär hur lång tid de ska gå mellan att lappan lyser och sedan slocknar. Detta är förinställt på en tusendels milisekund (1000).
9. Denna tid kan man ändra genom att exempelvis ta bort en nolla, eller fler. <img width="701" height="175" alt="kodbilnk" src="https://github.com/user-attachments/assets/3c4ee646-033c-4bfe-9a62-da5e33ffa93f" />

 Exmeplvis testade jag att ta bort alla nollor, detta gör att lampan lyser konstant istället för att blinka.<img width="977" height="189" alt="kodblink2" src="https://github.com/user-attachments/assets/bd68fe08-2f87-4182-8e92-ca0a61c9c7a8" />


kom ihåg att så fort du ändrar något behöver du tycka på verify och upload! Lycka till!










