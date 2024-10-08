# Міграція з OpenTX на EdgeTX за допомогою EdgeTX Buddy

Щоб оновитися з OpenTX до EdgeTX, вам необхідно мати встановлені як OpenTX, так і EdgeTX Companion на вашому комп'ютері. Ви можете завантажити OpenTX Companion за адресою: [https://downloads.open-tx.org/2.3/release/companion/](https://downloads.open-tx.org/2.3/release/companion/). Ви можете завантажити EdgeTX Companion за адресою: [https://github.com/EdgeTX/edgetx/releases](https://github.com/EdgeTX/edgetx/releases) (Ім'я файлу: edgetx-cpn-\[operation system]-\[version].zip)

### Зробіть резервну копію ваших моделей.

Увімкніть вашу апаратуру, перейдіть до **Налаштування радіо**, **Апаратне забезпечення** та прокрутіть донизу екрана, виберіть **Резервна копія EEPROM**. Якщо у вас немає цієї опції, то ваша апаратура не зберігає дані в **EEPROM**, і цей крок можна пропустити.&#x20;

<figure><img src="./.gitbook/assets/update14.png" alt=""><figcaption></figcaption></figure>

З увімкненою апаратурою підключіть її до комп'ютера за допомогою USB. Коли апаратура запитає про режим USB, виберіть **USB Storage**.&#x20;

З комп'ютера скопіюйте весь вміст вашої SD-картки в безпечне місце на вашому комп'ютері. Якщо ви коли-небудь вирішите повернутися до OpenTX, ви зможете використати ці файли знову. Якщо ви зробили резервну копію вашого **EEPROM** на попередньому кроці, перевірте папку **EEPROM**, щоб упевнитися, що там є останній файл резервної копії.

Запустіть OpenTX Companion.&#x20;

Виберіть іконку **Backup radio to file** з лівого боку екрана, як показано нижче. Виберіть місце для збереження (робочий стіл підійде) і дайте файлу описову назву.

<figure><img src="./.gitbook/assets/update1.png" alt=""><figcaption></figcaption></figure>

Після того, як файл буде збережено, закрийте OpenTX Companion.&#x20;

Видаліть вміст папки **Model** на вашій SD-картці, щоб вона була порожньою.

Витягніть апаратуру з комп'ютера та вимкніть її.

### Прошивка завантажувача і прошивки EdgeTX.

З вимкненою **апаратурою** підключіть її до комп'ютера за допомогою USB. Це підключить вашу **апаратуру** до комп'ютера в режимі DFU.&#x20;

{% hint style="info" %}
На Jumper T-Pro вам потрібно підключити **апаратуру**, утримуючи кнопку **Boot0**, щоб увійти в режим DFU.
{% endhint %}

Перейдіть на цей сайт: [https://buddy.edgetx.org/](https://buddy.edgetx.org/)

Виберіть **Firmware version** та **Radio model**, а потім натисніть **Flash via USB**.

<figure><img src="./.gitbook/assets/update2.png" alt=""><figcaption></figcaption></figure>

На наступному екрані виберіть пристрій **SMT32 Bootloader** та натисніть **Next**.

<figure><img src="./.gitbook/assets/update3.png" alt=""><figcaption></figcaption></figure>



Якщо пристрій **SMT32 Bootloader** не відображається, виберіть **Add New Device**. У спливаючому вікні виберіть **SMT32 Bootloader** та натисніть **Connect**.

<figure><img src="./.gitbook/assets/update4.png" alt=""><figcaption></figcaption></figure>

Після вибору пристрою **SMT32 Bootloader** та натискання **Next** ви побачите екран підтвердження для перевірки ваших налаштувань. Після того як ви переконаєтеся, що все вірно (версія, модель апаратури та пристрій), натисніть кнопку **Start Flashing**.

<figure><img src="./.gitbook/assets/update5.png" alt=""><figcaption></figcaption></figure>

EdgeTX Buddy зараз розпочне процес прошивки. На екрані з'явиться індикатор прогресу, який покаже вам хід виконання.

<figure><img src="./.gitbook/assets/update6.png" alt=""><figcaption></figcaption></figure>

Після завершення процесу прошивки виберіть посилання **setup your SD Card** на екрані завершення, яке перенесе вас на екран вмісту SD-картки.&#x20;

На цьому етапі завантажувач і прошивка EdgeTX були встановлені на вашу **апаратуру**. Наступним кроком є встановлення вмісту SD-картки.

### Підготовка SD-картки.

<figure><img src="./.gitbook/assets/update7.png" alt=""><figcaption></figcaption></figure>

Витягніть апаратуру з комп'ютера та увімкніть її. Ви повинні побачити екран завантаження EdgeTX на **апаратурі**, але все ще почуєте "Welcome to OpenTX". Це нормально – наступним кроком ми встановимо звуковий пакет EdgeTX разом з вмістом SD-картки.

Увімкнувши апаратуру, підключіть її до комп'ютера за допомогою USB та виберіть **USB Storage**, коли з'явиться ця опція на апаратурі. Натисніть на опцію **Select SD Card**, а потім перейдіть до вашої SD-картки EdgeTX.&#x20;

<figure><img src="./.gitbook/assets/update8.png" alt=""><figcaption></figcaption></figure>

SD-картка EdgeTX буде змонтована як USB-накопичувач на вашому комп'ютері. Виберіть USB-накопичувач (зверніть увагу, що файли OpenTX все ще там – це правильний варіант) і натисніть **Select folder**.

<figure><img src="./.gitbook/assets/update9.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Ваш комп'ютер може запитати у вас дозвіл для EdgeTX Buddy на доступ до вмісту SD-картки. Це нормально і необхідно, щоб Buddy міг змінювати файли на SD-картці.
{% endhint %}

На екрані вмісту SD-картки перевірте, чи версія прошивки та модель апаратури все ще вірні, потім виберіть бажану мову для звукового пакета. Натисніть **Apply Changes**. З'явиться вікно стану, яке покаже вам прогрес установки. Після завершення установки файлів вікно стану закриється.

<figure><img src="./.gitbook/assets/update10.png" alt=""><figcaption></figcaption></figure>

На цьому етапі у вас вже встановлені завантажувач EdgeTX, прошивка та вміст SD-картки. Останнім кроком є перенесення ваших моделей з OpenTX та їх установка на апаратуру. Тепер ви можете закрити EdgeTX Buddy.

### Відновлення ваших моделей з OpenTX.

Відкрийте EdgeTX Companion. Якщо ви ще цього не зробили, створіть профіль для вашої апаратури та переконайтеся, що він обраний як активний.

У верхньому лівому куті Companion виберіть **File**, потім **Open**, і виберіть файл резервної копії OpenTX, який ви створили на самому початку. З'явиться повідомлення про попередження. Натисніть **OK**.

<figure><img src="./.gitbook/assets/update11.png" alt=""><figcaption></figcaption></figure>

Ви побачите всі ваші моделі з OpenTX в EdgeTX Companion. Натисніть кнопку **Write models and Settings to Radio**. Вам буде повідомлено, що це перезапише всі моделі на вашій **апаратурі**. Натисніть **Yes**.**&#x20;

<figure><img src="./.gitbook/assets/update12.png" alt=""><figcaption></figcaption></figure>

Моделі та налаштування будуть записані на **апаратуру**. Після завершення з'явиться повідомлення. Натисніть **OK**. Витягніть **апаратуру** з USB-порту та закрийте EdgeTX Companion.

<figure><img src="./.gitbook/assets/update13.png" alt=""><figcaption></figcaption></figure>

### Вітаємо, ви успішно оновилися до EdgeTX!

Всі ваші моделі були оновлені до формату EdgeTX .yml, і у вас встановлений звуковий пакет EdgeTX. Тепер ви готові використовувати EdgeTX.

{% hint style="info" %}
_Unfortunately, it is not possible to copy over the setup for your widgets from OpenTX. They will have to be set up again manually in EdgeTX._
{% endhint %}

{% hint style="info" %}
Your Lua Scripts from OpenTX will still be on your SD Card. However, they may not all work with EdgeTX and may need to be re-installed to get them to work.  You can find a list of EdgeTX-compatible LUA scripts here: [https://github.com/EdgeTX/lua-scripts](https://github.com/EdgeTX/lua-scripts)
{% endhint %}
