ILI9327 TFT, BME280, DS3231: Display Date, Time, Temp, Humidity and Pressure, Heat Index, DST, With Min and Max Values Saved on Micro SD.

I have used an Arduino Mega 2560, with an Open Smart 3.2" TFT LCD Shield display, with ILI9327, a BME280 temperature, Humidity and Pressure sensor, a RTC DS3231 precision clock module, and the sketch that is attached.

Added the record, on micro SD card, of the date and minimum and maximum values of temperature, pressure and humidity of the last 24 hours, and backlight management.

Also added the Daylight saving time for Europe and USA.

Latest update: added Heat index value - that will be displayed in the upper right box - when Temperature and Humidity values will be equal or higher, respectively, to 27° and 40%.

The device works as follows:

1) after loading the sketch, or every time it connects to a power supply with 5 V output, the program verifies that the sensor is connected and initializes the micro SD card;

2) writes "SD" on the display and this writing will be canceled after the first refresh of the display;

3) starts displaying the date, hour and minutes, temperature and humidity, with the minimum and maximum values ​​recorded in the 24 hours;

4) if the temperature and humidity exceeds 27 degrees Celsius and 40%, it also displays the heat index in the upper right box;

5) at 23:59 it saves the Min and Max values ​​and the date on the micro SD and writes "Mem" on the display;

6) at 00:01, the program resets and restars the Arduino;

7) at 00:06 it switches off the backlighting, which will be reactivated at 07:00. The backlighting can be switched on using the push button switch. 
