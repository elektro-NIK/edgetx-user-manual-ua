# Спеціальні функції

Розділ **Special Functions** — це місце, де ви можете налаштувати спеціальні функції, включені в EdgeTX. Ці спеціальні функції додають додаткові можливості, виходячи за межі звичайного управління моделлю, такі як увімкнення режиму тренера, відтворення звуку, регулювання підсвічування або гучності радіоапаратури тощо. На екрані спеціальних функцій ви побачите всі налаштовані спеціальні функції, а також деякі з налаштованих опцій, такі як назва функції, перемикач активації, чи увімкнена функція, та інші параметри конфігурації.

<figure><img src="../../.gitbook/assets/bwsf1.png" alt=""><figcaption><p>Спеціальні функції</p></figcaption></figure>

### **Налаштування спеціальних функцій**

Щоб налаштувати спеціальну функцію, виберіть рядок бажаної спеціальної функції і натисніть кнопку **\[Enter]**. Потім прокрутіть за допомогою **\[Roller]**, щоб вибрати атрибут, який ви хочете редагувати (він буде підсвічений), і натисніть кнопку **\[Enter]** для редагування (тепер він буде мигати). Відредагуйте опцію, прокручуючи за допомогою **\[Roller]** та натискаючи кнопку **\[Enter]** для вибору бажаної опції. Після того, як всі опції налаштовані, натисніть кнопку **\[Return]**, щоб вийти з режиму редагування для спеціальної функції.

Всі спеціальні функції мають наведені нижче параметри конфігурації. Додаткові опції можуть бути додані залежно від вибраної функції. Дивіться розділ **Functions** нижче для цих додаткових опцій.

* **Trigger** — перемикач або тригер, який активує спеціальну функцію. Довге натискання на цю секцію дозволить швидко вибрати категорію перемикача та відфільтрувати результати. Ви можете вибрати такі фільтри: **Switches, Trims, Logical Switches, Other** та **Invert**.
* **Function** - функція, яка буде використовуватися. Дивіться нижче для опису функцій.
* **Enable** - перемикач для ввімкнення/вимкнення функції. Щоб активувати спеціальну функцію за допомогою перемикача, вона повинна бути увімкнена. Ця опція зазвичай є останньою в списку, представлена у вигляді чекбокса на крайньому правому боці екрана. Вимкнені спеціальні функції не працюватимуть незалежно від налаштованого положення перемикача.

### Functions (Функції)

Нижче наведені всі доступні функції в EdgeTX, їх призначення, а також додаткові параметри конфігурації, які будуть відображені при виборі функції.

**Adjust** (Adjust Global Variable) - Changes the value of the specified global variable.

* **Global var** - Виберіть глобальну змінну, яку ви хочете налаштувати.
* **Mode** - Виберіть режим для зміни глобальної змінної. Опції: **Constant**, **Mixer Source**, **Global var**, **Inc/Decrement**. Довге натискання кнопки **\[Enter]** дозволить вибрати режим.
  * **Constant** - Встановлює вказану глобальну змінну на визначене постійне значення.
  * **Mixer Source** - Встановлює вказану глобальну змінну на визначене значення джерела мікшера.
  * **Global Var** - Встановлює вказану глобальну змінну на визначене значення глобальної змінної.
  * **Inc/Decrement** -Збільшує/зменшує вказану глобальну змінну на зазначену величину.

**Audio Amp Off** (select radios) - Disables the Audio Amplifier so that no sound comes from the speaker, including annoying feedback or interferance. This option is only available on select radios.

**Backlight** - adjusts the screen contrast (LED screens) or OLED brightness (OLED screens) based on the source defined in the value dropdown.

**BgMusic** - Відтворює .wav файл, обраний у полі значення, в циклі, коли активовано. Файл має бути в папці SOUNDS/(language)/ на SD-карті.

**BgMusic II** - Тимчасово призупиняє відтворення .wav файлу, зазначеного в BgMusic

**Haptic** - Causes the radio to vibrate (haptic feedback) when enabled.

* **Value** - Type of vibration pattern. Options are: 0 - 3.
* **Repeat** - Frequency to repeat the vibration pattern. Options are **!-** (do not vibrate at startup even if the switch is active), **-** (vibrate once), **1** thru **60** (vibrate every xx seconds).

**Inst. Trim** (Instant Trim) - Sets all trims to the current values of their respective sticks.

**Lua** (Lua Script) - Executes the Lua script defined in the value field. The Lua script must be located in /SCRIPTS/FUNCTIONS/ folder on the SD card. Lua scripts that display information on the screen cannot be executed with this special function.

* **Value** - LUA script file to play from the SD card.
* **Repeat** - Frequency to repeat the Lua script. Options are: **ON** (repeat indefinitely as long as switch is active) or **1x** (once)

**Overr.=** (Channel Override) - Overrides the defined channel with the defined value.

* **CH** - Channel to be overridden
* **Value** - Value to replace the normal channel value. (Range -100 to +100)

**Play Sound** - Plays the sound selected in the value field when activated.

* **Value** - Sound to play. Possible values are **Beep1/2/3, Warn1/2, Cheep, Ratata, Tick, Siren, Ring, SciFi, Robot, Chirp, Tada, Crickt, AlmClk**. _Note: SD card sound pack is not required._
* **Repeat** - Frequency to repeat the sound. Options are **!-** (do not play at startup even if the switch is active), **-** (play once), **1** thru **60** (play every xx seconds).

**Play Track** - Plays the .wav sound file selected in the value field when activated.

* **Value** - .wav sound file to play from the SD card.
* **Repeat** - Frequency to repeat the track. Options are **!-** (do not play at startup even if the switch is active),  **-** (play once), **1** thru **60** (play every xx seconds).

**Play Val -** Announces the value of the selected element in the value field.

* **Value** - The source for the value to announce. It can be an input, stick, pot, slider, trim, physical and logical switch, trainer import channel value, global variable, telemetry sensor or channel.
* **Repeat** - Frequency to repeat the announcement. Options are **!-** (do not announce at startup even if the switch is active), **-** (announce once), **1** thru **60** (announce every xx seconds).

**Push CS** - (Push Customizable Switch) (select radios) - Presses the designated switch for the designated period of time.

* **Switch** - Which customizable switch to press
* **Time** - How long to press the customizable switch for. Options are 0.0 to 25.5 seconds. Input to the button will be ignored while this time is being served, allowing this to automate a press of the button, and block input (and retrigger of the function) until the time has elapsed.&#x20;

**RacingMode** - Увімкнення режиму перегонів (низька затримка) для приймачів FrSky Archer RS. Режим перегонів також повинен бути увімкнений у налаштуваннях зовнішнього RF модуля.

**Reset** (Reset Timer)- Resets the timer or telemetry specified in the value back to their initial values.

* **Reset** - Options are **Tmr 1, Tmr 2, Tmr 3, All,** and **Telemetry.** See [**Reset Telemetry**](../main-view/reset.md) for more information on what data is reset for each option.

**RGB Led** (select radios) - Run the selected LED related Lua script to animate RGB leds on the handset.

* **Value** - LUA script file to play from the SD card (in the /**SCRIPTS/RGBLED** folder).
* **Repeat** - Frequency to repeat the Lua script. Options are: **ON** (repeat indefinitely as long as switch is active) or **1x** (once).

**Screenshot** -  Creates screenshot as a .bmp file in the SCREENSHOT folder on the SD Card.

**SD Logs** - Creates a log .csv file of the radio and telemetry values in the LOGS folder on the SD Card. The radio will create a new entry into the log file based on the frequency configured in the **Value** setting.  The value options are **0.0s** - **25.5s** (Note: 0.0 effectively disables this option). Each time the function is activated, the radio will create a new log file provided that the function is activated at least as long as the value setting. **Note:** Logging will not start if SD card has less than 50mb of free space.&#x20;

**Set** (Set Timer) - Sets the specified timer to the specified value.

* **Timer** - Options are **Tmr 1, Tmr 2, Tmr 3**
* **Value** - The range is 00:00:00 to 08:59:59&#x20;

**SetFailsafe** - Sets the custom failsafe values for the configured RF module (Internal/External) to the current stick position when activated. For this option to work, the Failsafe mode for the RF module must be set to **custom**.

**Set Screen** - Sets the telemetry screen or return to main view screen.

* **Value** -  0 - 4. When set to 0, the normal main view will be loaded. When set to 1 - 4, the corresponding telemetry screen will be shown (if configured).
* **Repeat** - Options are **!-** (do not trigger at startup even if the switch is active) and - (trigger once).

**Trainer -** Enables trainer mode.

* **Value** - Specifies which controls will be given over to the student. Options include **Axis** (all sticks/primary inputs), **Rud** (Rudder), **Ele** (Elevator), **Thr** (Throttle), **Ail** (Aileron), and **Chans** (all channels).&#x20;

**Vario** - Enables the variometer beeping sound for the ascent and descent of the model.

**Volume** - Changes the radio volume. The change source is specified in the Volume dropdown.

Натиснення кнопки **\[PAGE>]** перенесе вас на екран **Телеметрії.**
