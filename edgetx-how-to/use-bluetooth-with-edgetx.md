# Використання Bluetooth з EdgeTX

Підтримка Bluetooth в EdgeTX обмежується:

* Bluetooth режим тренера&#x20;
* Bluetooth потокова передача телеметрії

Наступні опції Bluetooth не підтримуються:

* Bluetooth аудіо
* Бездротовий доступ до файлів і їх передача
* Bluetooth джойстик

### Прошивка

To use Bluetooth, if your radio does not come as standard with a Bluetooth module fitted (thus meaning the Bluetooth option should already be enabled in the firmware) you will need a custom compiled version of EdgeTX that needs to be built with the **BLUETOOTH=YES** CMake flag. You can create customized versions of EdgeTX using the CloudBuild tab on the[ EdgeTX Buddy website](https://buddy.edgetx.org/).

Після встановлення правильної версії прошивки EdgeTX у вашій радіоапаратурі опції конфігурації Bluetooth будуть доступні на сторінці **Апаратне забезпечення** (**Hardware)** в **Налаштуваннях апаратури**.

### Апаратне забезпечення (Hardware)

Єдиними стандартними модулями Bluetooth, які підтримуються EdgeTX, є:

[FrSky Bluetooth Module](https://de.aliexpress.com/item/4001192317700.html?gatewayAdapt=glo2deu)

[FrSky ACCESS PARA Wireless Module](https://www.horusrc.com/en/frsky-horus-x10-para-wireless-module.html)

Ви також можете створити власний модуль Bluetooth, придбавши розробницький комплект ESP32 і прошивши його прошивкою з наступного проєкту:[ https://btwifimod.gitbook.io/untitled/getting-started/hardware](https://btwifimod.gitbook.io/untitled/getting-started/hardware)

### **Застосування телеметрії**

Додаток [INAV Telemetry Viewer app](https://play.google.com/store/apps/details?id=crazydude.com.telemetry) можна використовувати на вашому смартфоні Android для перегляду даних телеметрії через Bluetooth.

### Інші важливі зауваження:

* Bluetooth підтримується лише на радіоапаратурах, які мають принаймні один послідовний порт AUX.
* Опція компіляції Bluetooth зарезервує один AUX порт (на радіоапаратурах з 2 AUX портами, AUX2 зарезервований для Bluetooth), і він НЕ буде доступний у звичайному інтерфейсі користувача для інших цілей.
* Bluetooth-інструктор або телеметрія EdgeTX не мають нічого спільного з функціональністю Bluetooth внутрішнього або зовнішнього RF модуля.
* На цей момент Bluetooth EdgeTX НЕ може використовуватися для функціональності Bluetooth джойстика.
