# Налаштування апаратури

<figure><img src="../../.gitbook/assets/bw128_radio_setup_top.png" alt=""><figcaption><p>Налаштування апаратури</p></figcaption></figure>

На екрані **Налаштування апаратури** ви можете налаштувати основні параметри своєї радіоапаратури. Він містить такі параметри:

**Дата** - поточна дата. Ця дата використовується для файлів журналу SD карти.

**Час** - поточний час. Цей час використовується для файлів журналу SD карти.

**Batt. діапаз.** - встановлює максимальну та мінімальну напругу для вимірювача батареї. Це слід встановити залежно від типу акумулятора, який ви використовуєте.

<figure><img src="../../.gitbook/assets/bw128_radio_setup_sound.png" alt=""><figcaption><p>Sound Settings</p></figcaption></figure>

### **Звук**

**Режим** – налаштовує коли відтворюються звуки.

* **Усі** – звукові сигнали під час натискання кнопок і звукові сигнали під час сповіщень або попереджень.
* **Без кноп.** – тиша під час натискання кнопок або обертання колеса прокручування, але відтворює звуки, коли є сповіщення або попередження. Також відтворює звуки, викликані спеціальними функціями.
* **Тривога** – відтворює лише звуки тривоги або попередження. Також відтворює звуки, викликані спеціальними функціями.
* **Тиша** – звукові сигнали та звуки не відтворюються.

**Гучність** - головний регулятор гучності радіоапаратури.

**Гучність сигналу** - пояснення не вимагається

**Довжина сигналу** - пояснення не вимагається

**Тон сигналу** - пояснення не вимагається

**Гучність Wav** – гучність сповіщень і попереджень, а також звуків, які відтворюються за допомогою спеціальної функції **Грати трек**.

**Фон гучність -** гучність фонових файлів .wav (музика), які відтворюються за допомогою спеціальної функції **Фон.Муз.**.

**Startup sound -** When enabled (default setting), plays the "Welcome to EdgeTX" sound on radio startup. The relevant file is located in `/SOUNDS/??/SYSTEM/hello.wav` (where \`??\` represents the two letter directory for your sound pack).&#x20;

<figure><img src="../../.gitbook/assets/bwRadioSetup3 (1).png" alt=""><figcaption><p>Налаштування варіометра</p></figcaption></figure>

### **Варіо (варіометр)**

**Гучність** - гучність звукових сигналів варіометра

**Тон низ** - тон нульового (низького) значення

**Тон верх** - тон максимального (високого) значення

**Повтор низ** - час до повторення сигналу в мілісекундах

{% hint style="info" %}
Примітка: щоб варіометр працював, його потрібно ввімкнути за допомогою спеціальної або глобальної функції Варіо. Дивіться [Спеціальні функції](../../color-radios/model-settings/special-functions.md) для отримання додаткової інформації про те, як це налаштувати.
{% endhint %}

<figure><img src="../../.gitbook/assets/bwRadioSetup4.png" alt=""><figcaption><p>Налаштування вібрації</p></figcaption></figure>

### Вібро

**Режим** - налаштовує, коли апаратура вібрує.

* **Усі -** вібрує під час натискання кнопок і під час сповіщень або попереджень.
* **Без кноп. -** відсутня вібрація під час натискання кнопок або обертання колеса прокручування, але вібрація присутня під час сповіщень або попереджень
* **Тривога -** вібрує лише для сигналу тривоги або попередження.
* **Тиша -** вібрація відключена.

**Довжина** - тривалість вібрації.

**Інтенсивність** - сила вібрації.

<figure><img src="../../.gitbook/assets/bw128_alarms.png" alt=""><figcaption><p>Налаштування сигналів</p></figcaption></figure>

### Сигнали

**Batt розрядж.** - напруга, щоб викликати сигнал про низький рівень батареї.
**Бездіяльність** - час для активації попередження про неактивність.
**Пам'ять закінч.** - увімкнути/вимкнути попередження про брак пам’яті.
**Звук вимк.** - візуальне попередження "сигнали вимкнені" відображається, коли передавач увімкнено, якщо режим звуку встановлено на беззвучний.
**RSSI вимк.** - перевіряє, чи приймач все ще підключений до апаратури під час спроби вимкнення. У разі виявлення видає звукове та візуальне сповіщення.
**Trainer Shutdown** - Checks if there is a trainer signal still active on attempted shutdown. Makes an audio and visual alert if one is detected.&#x20;

<figure><img src="../../.gitbook/assets/bw128_backlight.png" alt=""><figcaption><p>Налаштування підсвічування</p></figcaption></figure>

### Підсвічування

**Режим**

* **OFF** – завжди вимкнено.
* **Кноп.** – вмикається при натисканні кнопок.
* **Ctrl** – вмикається, коли використовуються стіки, перемикачі та потенціометри.
* **Обидві** – вмикається, коли використовуються кнопки, стіки, перемикачі та потенціометри.
* **ON** – завжди увімкнено.

**Тривалість** – тривалість увімкненого підсвічування в секундах. Мінімальне значення - 5 секунд. Максимальне значення становить 600 секунд.

**Яскравість** - регулює рівень яскравості підсвічування екрана.

**Попередж.** - підсвічування вмикається, коли є сигнали або попередження.

<figure><img src="../../.gitbook/assets/bwRadioSetup7.png" alt=""><figcaption></figcaption></figure>

**Контраст** - для LCD дисплеїв регулює налаштування контрастності екрана. Для OLED дисплеїв регулює рівень яскравості OLED.

<figure><img src="../../.gitbook/assets/bw128_radio_setup_misc1.png" alt=""><figcaption><p>Misc Settings</p></figcaption></figure>

### Misc Settings

**Заставка** - тривалість відображення заставки.

**Звук запуску** - вмикає/вимикає звук запуску.

**Pwr On затримка** - затримка між натисканням кнопки живлення і моментом увімкнення апаратури. Варіанти: **0s, 1s, 2s, 3s**

**Pwr Off затримка** - The delay between when the power button is pushed and when the radio shuts off. The options are: **0s, 1s, 2s, 3s, 4**s. _It is recommended to set at least a 1s delay in order to prevent the radio from being shut off in the case of an accidental button press._

**Power Auto Off** - If enabled (not enabled by default), if the handset is left inactive, with no trainer or telemetry link active, it will automatically turn off after the configured duration. You can select from **0** (disabled) up to **255** (minutes).

**Power ON/OFF Haptic** - If enabled (enabled by default), after the power on and power off delays have been served, there will be a haptic vibration to indicate the radio is powering on or off.&#x20;

**ID користувача** (select transmitters) -  Custom registration ID used only for users with ISRM internal RF modules, or on transmitters that support FrSky ACCESS external modules. If not configured manually, a random value will be used.

<figure><img src="../../.gitbook/assets/bw128_radio_setup_gps.png" alt=""><figcaption><p>GPS Settings</p></figcaption></figure>

### **GPS**

**Часовий пояс** - The time offset from UTC where the radio is being used. Can be configured in 15 minute increments.

**Підлашт. RTC** - Adjust the transmitter's real-time clock to match the time determined by the GPS.

**GPS формат** - The GPS coordinate format that will be displayed.

<figure><img src="../../.gitbook/assets/bw128_radio_setup_misc2.png" alt=""><figcaption></figcaption></figure>

**Misc Settings**

**Код країни** - Used by some RF modules to ensure adherence to local regulatory RF requirements. Options are **America, Japan, Europe.**

**Мова голосу** - Language for the voice pack. This setting and the voice pack folder on the SD card must match for the sounds to be played.

**Одиниці** - Units of measure. Options are **metric** or **imperial**.

**PPM одиниці** - Level of accuracy for PPM values are displayed. Options are **0.-** , **0.0** or **us** (microseconds).

**Затримка відтвор.** (switch middle position) - The minimum time in milliseconds a switch must be in the middle position before a special function will get activated. This is used to prevent the middle position from being activated on a three-position switch when switching from low position to high position.

<figure><img src="../../.gitbook/assets/bwRadioSetup9.png" alt=""><figcaption></figcaption></figure>

**Режим USB** - Sets the default action when a USB cable is plugged into the USB data port and the radio is powered on. Options are: **Ask** (ask on connect, the default), **Joyst** (Joystick) , **SDCard** (Storage), and **Serial**.

**Порядок каналів** - The default channel order for new models and the trainer screen. The letters stand for: **A** = Aileron, **E** = Elevator, **T** = Throttle, **R** = Rudder. Changing this setting does not affect existing models. On Surface Radios, the letters stand for **S**=Steering, **T**=Throttle.

**ОбКодРеж** (Режим обертального енкодера) (select radios)- Sets the direction of the rotary encode for the Roller. The options are:

* **Normal** (default)
* **Inverted** = Reverses the direction of the roller
* **V-I H-N** = Vertical Inverted, Horizontal Normal
* **V-I H-A** = Vertical Inverted, Horizontal Alternate (Inverted)
* **V-N E-I** = Vertical Normal, Edit Inverted (inverted when editing text)

**Режим** - The stick mode that will be used for the transmitter. Defined by what actions the left stick takes. The options are:

<table><thead><tr><th width="181">Option</th><th width="168">Left stick H</th><th width="149">Left stick V</th><th width="133">Right stick H</th><th>Right stick V</th></tr></thead><tbody><tr><td>1: Left = Rud+Ele</td><td>Rudder (Yaw)</td><td>Elevator (Pitch)</td><td>Aileron (Roll)</td><td>Throttle</td></tr><tr><td>2: Left = Rud+Thr</td><td>Rudder (Yaw)</td><td>Throttle</td><td>Aileron (Roll)</td><td>Elevator (Pitch)</td></tr><tr><td>3: Left = Ail+Ele</td><td>Aileron (Roll)</td><td>Elevator (Pitch)</td><td>Rudder (Yaw)</td><td>Throttle</td></tr><tr><td>4: Left = Ail+Thr</td><td>Aileron (Roll)</td><td>Throttle</td><td>Rudder (Yaw)</td><td>Elevator (Pitch)</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/bw128_radio_setup_enabled_features.png" alt=""><figcaption><p>Enabled Features</p></figcaption></figure>

### Enabled Features

The **Enabled Features** section of Radio Setup allows you to configure the _**Global**_ _**settings**_ for which tabs are visible in the Radio Setup and Model Settings area of EdgeTX. The configuration setting for the active model will show to the right of the checkbox. The model configuration will override the global configuration (which will be indicated by the "Off" and "On" shown next to any model level overrides).&#x20;

{% hint style="info" %}
_**Note:**_ Turning off a tab only hides the tab and does not change the items already configured in that tab.

**EXCEPTION:** Turning off the Global / Special Functions tab will disable configured global / special functions for that model.
{% endhint %}

Pressing the **\[PAGE>]** button will take you to the **Global Functions** screen.
