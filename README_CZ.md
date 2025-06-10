![Prusa Cup Heater](https://github.com/LaskaKit/LaskaKit_Prusa_CupHeater/blob/main/img/prusacupheater.png)

Projekt Průša Cup Heater – jednoduchý ohřívač pro školy i nadšence
-------------------------------------------------------------------

Projekt **Průša Cup Heater** je určen především pro školy, zájmové kroužky a kluby, ale své uplatnění najde i u dospělých makerů a bastlířů. Cílem je vytvořit jednoduchý, snadno ovladatelný ohřívač kafe nebo čaje, který využívá dostupné komponenty a je tak vhodný i pro začátečníky.

Základní komponenty a jejich funkce
-----------------------------------

*   **3D tištěná krabička** – slouží jako základ pro sestavení projektu (doporučujeme materiál PETG, ASA, ABS, PC-ABS a jim podobné).
    
*   **Heatbed tile** – vyhřívací podložka, původně určená pro 3D tiskárny Průša XL.
    
*   **Deska microESPswitch s ESP32-C3** – malá deska s výkonnými tranzistory pro spínání až čtyř zátěží (například vyhřívací podložky) pomocí GPIO pinů (CH0 až CH3, např. GPIO0, GPIO1, GPIO4, GPIO5).
    
*   **Teplotní čidlo DS18B20** – digitální čidlo pro měření teploty, připojené přes GPIO3.
        
*   **OLED displej** – zobrazuje aktuální teplotu a stav systému, připojený přes I2C sběrnici (SDA – GPIO18, SCL – GPIO19).
    
*   **Napájení** – díky čipu pro USB PD je možné napájet systém napětím 15 V nebo 20 V přes USB-C konektor.
    

Jak projekt funguje
-------------------

Deska **microESPswitch** umožňuje snadné řízení až čtyř zátěží díky výkonným tranzistorům. Pro připojení periferií (například OLED displeje) je k dispozici uŠup konektor pro I2C a SPI komunikaci. Teplotní čidlo DS18B20 se připevní k vyhřívací podložce a napájení podložky se připojí ke kanálu CH3 (řízen z GPIO5).

Vzorkový kód využívá knihovnu **WiFiManager**, která po spuštění vytvoří vlastní WiFi hotspot. Uživatel se připojí mobilním telefonem a v prohlížeči snadno nastaví požadovanou teplotu podložky. Systém udržuje teplotu v nastaveném rozsahu (např. 55–65 °C) a automaticky reguluje výkon podle aktuální teploty.

LED indikace a ovládání
-----------------------

*   **Bílá LED** – zařízení není připojeno k WiFi.
    
*   **Zelená LED** – zařízení je připojeno k WiFi a připraveno k použití.
    
*   **Modrá LED** – ohřívač je vypnutý.
    
*   **Červená LED** – ohřívač je zapnutý.
    

OLED displej zobrazuje aktuální teplotu, stav ohřívače a další užitečné informace. Všechny funkce lze ovládat přes webové rozhraní nebo přímo na desce.

Sestavení a úpravy
------------------

Projekt vyžaduje pájení z USB adaptéru, který umožuje napětí 15V nebo 20V a sestavení podle přiloženého návodu. Hotový program je k dispozici na GitHubu a může být libovolně upravován podle potřeb uživatele.

> **Tip:** Pokud chcete projekt využít ve škole nebo v kroužku, doporučujeme postupovat podle návodu a použít připravený vzorový kód, který je optimalizován pro jednoduché ovládání a snadné úpravy.

**Zdroje a odkazy:**

*   **GitHub s kódem:** [LaskaKit/LaskaKit\_Prusa\_CupHeater](https://github.com/LaskaKit/LaskaKit_Prusa_CupHeater/tree/main/SW/Prusa_cup_heater)
    
*   **Návod (PDF):** https://github.com/LaskaKit/LaskaKit_Prusa_CupHeater/blob/main/Tutorial_CupHeater.pdf
    
*   **Původní nápad:** @KutilDomaci a @Martin\_Velisek na sociální síti X/Twitter
    

Projekt **Průša Cup Heater** je ideální volbou pro výuku elektroniky, programování a automatizace na školách i v kroužcích, ale také pro domácí kutily, kteří chtějí experimentovat s moderními technologiemi.
