---
опис: поточна версія для всіх об’єднаних Pull Requests станом на 31/05/2024 (v2.10.1)
---

# Опис змін із v2.9

Нижче наведено короткий перелік змін, які впливають на інтерфейс користувача та/або функціонування EdgeTX. Він не охоплює всі виправлення помилок. Щоб отримати повний список змін (включаючи виправлення помилок), прочитайте примітки до випуску.

### **Апаратури із кольоровим екраном**

* Підтримка нових апаратур
  * Flysky PL18
  * Flysky PL18 EV
  * Jumper T15
* Загальні зміни
  * Мікшер тепер працює на частоті 1000 Гц у режимі USB-джойстика (потрібен для учасників F.Sim), також відображає час роботи мікшера на екрані статистики/налагодження.
  * Незначні покращення інтерфейсу користувача на багатьох сторінках для кращого вигляду та узгодженості.
  * Видалено фон завантажувача, щоб зробити текст більш читабельним.
  * Стандартний екран завантаження оновлено новим логотипом EdgeTX і інформацією про версію EdgeTX.
  * Меню **Джерело** було оптимізовано для полегшення сенсорного використання та сортування.
  * Меню **Джерело** тепер відображатиме номер і назву глобальної змінної.
  * Додано світлодіодну анімацію зарядки для PL18 і PL18EV.
* [Сторінка інтерфейсу користувача](color-radios/user-interface/)
  * Кнопки **Система \[SYS]** і **Моделі \[MDL]** мають різні [функціональні можливості](color-radios/user-interface/#additional-system-and-model-button-functionalities) залежно від екрану, на якому вони використовуються.
  * [Перемикачі триммерів] (color-radios/user-interface/trim-navigation.md) на NV14 та EL18 тепер можна використовувати для навігації по меню.
  * Додано [апаратні клавіші швидкого доступу до віртуальної текстової та цифрової клавіатур](color-radios/user-interface/virtual-keyboards.md).
* [Керування моделями](color-radios/select-model.md)
  * Додано 3 додаткові макети для списку моделей.
  * Оновлено розмір і форму рамок зображень моделі. Також, тепер назва моделі відображається поверх зображення замість обрізання зображення.
  * Кнопки **Нова мітка** і **Нова модель** замінено просто кнопкою **Нова** з опціями **Модель** або **Мітка**.
  * Замінено заплутані піктограми сортування моделей простим текстовим спадним меню.
  * Додано єдиний параметр вибору для міток моделей, а також логіку фільтрації міток І/АБО (можна налаштувати на екрані [Налаштування радіо](color-radios/radio-settings/radio-setup/additional-radio-settings.md)).
* [Налаштування моделі](color-radios/model-settings/model-setup/)
  * Увімкнені таймери відображатимуться як виділені на екрані **Налаштування моделі**..
  * &#x20;MIN можна використовувати як джерело. Якщо вибрано, завжди повертатиметься -100.
  * До розділу **Передпольотні перевірки** додано **Інтерактивний** **Чекліст**. Дозволяє користувачам додавати інтерактивні чекбокси до відображених чеклістів.
* [Режими польоту](color-radios/model-settings/flight-modes.md)
  * Невикористані триммери тепер можна налаштувати як 3-позиційні миттєві перемикачі.
* [Мікшери](color-radios/model-settings/inputs-mixes-and-outputs/mixes.md)
  * Додано настроювану точність для **уповільнення** для встановлення 10 мс або 100 мс.
* [Глобальні змінні](color-radios/model-settings/global-variables.md)
  * Додано параметр **Спливаюче вікно**, який, коли ввімкнено, відображає спливаюче повідомлення, коли значення глобальної змінної змінюється новим.
* [Спеціальні функції](color-radios/model-settings/special-functions.md)
  * Усі спеціальні функції тепер мають прапорець **Увімкнути**.
  * Спеціальні функції можна ввімкнути/вимкнути, не відкриваючи меню редагування.
  * Додано перемикач віртуального тренера (**Tnr**), який можна вибрати як перемикач для активації спеціальної функції. Перемикач увімкнено, коли активне з'єднання тренера.
  * Значення спеціальної функції **Підсвітка** обмежені значеннями On/Off, налаштованими в **Налаштування апаратури -> Яскравість екрану.**
* [Телеметрія](color-radios/model-settings/telemetry/)
  * EdgeTX відтворить "Телеметрію підключено", коли телеметрія підключиться вперше під час польоту.
* [SD-карта](color-radios/radio-settings/sd-card.md)
  * Користувачі можуть налаштувати спеціальне зображення вимкнення, додавши спеціальний `shutdown.png` до папки **IMAGES**.
  * Параметр **Перегляд тексту** тепер доступний для файлів .lua
* [Налаштування апаратури](color-radios/radio-settings/radio-setup/)
  * У **Налаштуваннях GPS** оновлено параметр **Часовий пояс**, щоб дозволити налаштування з 15-хвилинними інтервалами.
  * Додано опцію **Заставка**, яка встановлює тривалість відображення заставки.
  * Додано опцію **Звук запуску**, яка вмикає чи вимикає звук запуску.
  * Додано параметр **Одиниці PPM** - раніше це був варіант збірки.
  * У розділі **Увімкнені функції** додано поточні параметри конфігурації для активної моделі праворуч від перемикача.
* [Апаратне забезпечення](color-radios/radio-settings/hardware.md)
  * Аналогові входи, такі як потенціометри та повзунки, тепер можна налаштувати як **Перемикач**, **Вісь X** або **Вісь Y**. Крім того, їх також можна налаштувати так, щоб вони були _**інвертовані**_.
  * EdgeTX тепер визначатиме під час виконання, чи доступний послідовний порт, щоб дозволити тренер SBUS у відсіку зовнішнього модуля. Якщо так, параметр конфігурації буде доступним.
* [Параметри екрана](color-radios/screen-settings/)
  * На верхній панелі інформація про апаратуру, дата/час і внутрішній GPS тепер є настроюваними віджетами, що дозволяє налаштувати 6 слотів для віджетів.
  * Якщо вибрати порожній віджет, опція «Вибрати віджет» більше не відображатиметься, а натомість перейде прямо до меню вибору віджета.
  [Віджети](color-radios/screen-settings/widgets.md)
  * Додано опцію вирівнювання для віджета **Текст**, щоб вирівняти текст віджета **Ліворуч**, **Центр** або **Праворуч**.
* Сповіщення
  * Попередження буде відображено, якщо ви спробуєте вимкнути апаратуру, коли підключення тренера все ще активне.

### Monochrome Screen Radios

*   New Hardware Support

    * Jumper T-Pro V2
    * Jumper T-14
    * Jumper T-20
    * Flysky Gimbal support for Jumper T-20
    * Flysky Gimbal support for Frsky X9D+2019
    * RadioMaster Pocket
    * RadioMaster MT12


* General Changes
  * The mixer now runs at 1000Hz when in USB Joystick mode (needed for F.Sim competitors), also displays mixer run time in statistic/debug screen.
  * Splash Screen updated with new EdgeTX Logo
  * Radios with unused flexible serial port will now automatically be defined as **AUX Serial** (MT12).
* [Main View](bw-radios/main-view/)
  * Added new view for surface radios with throttle and steering instead of sticks.
* [Model Settings](bw-radios/model-select/)
  * Added **C-Interact** option to Pre-start checks section. Allows users to add Interactive Checkboxes to displayed checklists.
  * On surface radios (EX: MT-12), the throttle trim no longer has an effect on the reverse throttle range.
* [Flight Modes](bw-radios/model-select/flight-modes.md)
  * Unused trim switches can now be configured to function as a 3 position momentary switch.
* [Mixes](bw-radios/model-select/inputs-mixes-and-outputs/mixes.md)
  * Added configurable precision for **slow up/dn** to be set to either 10ms or 100ms.
* [Telemetry](bw-radios/model-select/telemetry/)
  * EdgeTX will play "Telemetry connected" when telemetry connects for the first time of the flight.
  * The number of configured sensors will be displayed in **parentheses** when the sensor list is collapsed.
* [Special Functions](bw-radios/model-select/special-functions.md)
  * All special functions now have the **enable** checkbox.
  * OLED screen brightness can be controlled with **Backlight** special function.
  * Added virtual trainer switch (**Tnr**) that can be selected as switch to activate a special function. Switch is ON when the trainer link is active.
  * Added RGB Led special function to enable and change LED behavior.
* [Radio Setup](bw-radios/radio-settings/radio-setup.md)
  * In **GPS settings**, updated the **Time Zone** option to allow configuration in 15 minute intervals.
  * Added the **Startup Sound** option which toggles whether to enable/disable startup sound.
  * Added **PPM Units** option- Previously this was a build option.
  * In the **Enabled Features** section, added the current configuration setting for the active model to the right of the checkbox.
  * Added the **Rotary Encoder Mode** - **V-N E-I** = Vertical Normal, Edit Inverted (inverted when editing text)
* [Hardware](bw-radios/radio-settings/hardware.md)
  * Analog inputs, such as pots and sliders can now be configured as a **Switch**, **Axis X** or **Axis Y**. Additionally, they can also be configured to be inverted.
  * EdgeTX will now detect at runtime if a serial port is available to allow for SBUS trainer on the external module bay. If so, the configuration option will be available.
* Alerts
  * Warning will be displayed if you try to shut down the radio while the trainer connection is still active.
