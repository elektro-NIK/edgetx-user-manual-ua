# Logical Switches

Logical Switches are virtual two-position switches whose values (ON/OFF or +100/-100) are based on the evaluation (true/false) of a defined logical expression. Once configured, logical switches can be used anywhere in EdgeTX that a physical switch can be defined.

The **Logical Switches** page in Model Settings shows you all the configured logical switches as well as an overview of their configured options.

<figure><img src="../../.gitbook/assets/colorlcd_model_ls.png" alt=""><figcaption><p>Екран логічних перемикачів</p></figcaption></figure>

Selecting the **+** button will allow you to select an unused logical switch to configure.

Selecting a configured logic switch will give you the following options:

* **Edit** - Opens the Logical Switches configuration page for the selected logical switch.
* **Copy** - Copies the selected logical switch
* **Paste** - Pastes a copied logical switch onto the selected logical switch. Note: it will overwrite the selected logical switch.
* **Clear** - Deletes all configuration options for the selected logical switch.

<figure><img src="../../.gitbook/assets/colorlcd_model_ls_edit.png" alt=""><figcaption><p>Екран налаштування логічних перемикачів</p></figcaption></figure>

After selecting to edit a logical switch, you will have the following configuration options:

* **Func** — Логічна функція, яку ви хочете використовувати. Див. [Логічні функції перемикачів](logical-switches.md#logical\_switches\_judgment\_conditions\_and\_logical\_expressions) нижче для опису можливих функцій.
* **V1** — Перша змінна у виразі для оцінки.
* **V2** — Друга змінна у виразі для оцінки.
* **AND перемикач** — Перемикач, який має бути активним, щоб дозволити оцінку та активацію логічного перемикача.
* **Duration** — Тривалість, протягом якої логічний перемикач залишатиметься активним (істинним) після досягнення умов активації. Якщо встановлено 0.0, то логічний перемикач залишатиметься активним (істинним).
* **Delay** — Затримка між моментом досягнення умов активації та моментом, коли логічний перемикач змінює стан на активний (істинний).
* **Persistence** **(Sticky Switch only)** - Preserves the value of the sticky switch when turning the radio off, or changing models, and restores the saved value on power on or selecting the model again.

### Logical Switch Functions <a href="#logical_switches_judgment_conditions_and_logical_expressions" id="logical_switches_judgment_conditions_and_logical_expressions"></a>

In the expression, a and b represent sources (sticks, switches, etc.), and x represents the constants (values) to be compared.

<table><thead><tr><th width="137">Вираз</th><th width="606">Опис</th></tr></thead><tbody><tr><td>a=x</td><td>Істинно, коли джерело V1 точно відповідає константі V2.</td></tr><tr><td>a~x</td><td>Істинно, коли джерело V1 приблизно дорівнює константі V2.</td></tr><tr><td>a>x</td><td>Істинно, коли джерело V1 більше за константу V2.</td></tr><tr><td>a&#x3C;x</td><td>Істинно, коли джерело V1 менше за константу V2.</td></tr><tr><td>|a|>x</td><td>Істинно, коли абсолютне значення джерела V1 більше за константу V2.</td></tr><tr><td>|a|&#x3C;x</td><td>Істинно, коли абсолютне значення джерела V1 менше за константу V2.</td></tr><tr><td>AND</td><td>Істинно, коли обидва джерела V1 і V2 є ІСТИННИМИ.</td></tr><tr><td>OR</td><td>Істинно, коли будь-яке з джерел V1 або V2 є ІСТИННИМ.</td></tr><tr><td>XOR</td><td>Істинно, коли значення джерел V1 та V2 не збігаються.</td></tr><tr><td>Edge</td><td>Моментально істинно, коли джерело V1 було активним протягом заданого періоду часу, а потім деактивувалося. Перше поле часу (T1) для V1 є мінімальною тривалістю активності, необхідною для активації логічного перемикача. Друге поле часу (T2) є максимальною тривалістю активності V1, щоб логічний перемикач активувався. Якщо T2 встановлено на --, логічний перемикач буде істинним, незалежно від того, як довго було активним V1. Якщо T2 встановлено на 3, то якщо V1 буде активним більше ніж 3 секунди, логічний перемикач не стане істинним при деактивації джерела. Якщо T2 встановлено на &#x3C;&#x3C;, логічний перемикач стане істинним, коли часові умови T1 будуть виконані без деактивації джерела V1.</td></tr><tr><td>a=b</td><td>Істинно, коли джерело V1 дорівнює джерелу V2.</td></tr><tr><td>a>b</td><td>Істинно, якщо джерело V1 більше за джерело V2.</td></tr><tr><td>a&#x3C;b</td><td>Істинно, якщо джерело V1 менше за джерело V2.</td></tr><tr><td>△>x</td><td>Моментально істинно кожного разу, коли значення джерела V1 змінюється більше, ніж на значення V2.</td></tr><tr><td>|△|>x</td><td>Моментально істинно щоразу, коли абсолютне значення джерела V1 змінюється більше, ніж на величину, вказану константою V2.</td></tr><tr><td>Timer (Таймер)</td><td>Моментально істинно кожні xxx секунд. Аргумент V1 — це тривалість, протягом якої логічний вимикач є істинним (активним). Аргумент V2 — це час між активаціями логічного вимикача. Цикл таймера повторюється, доки визначений вимикач активний.</td></tr><tr><td>Stky (Sticky)</td><td>«Прилипає» як істинний після того, як перемикач V1 стає активним (істинним) і залишається активним (істинним) незалежно від положення V1, поки не активується перемикач V2 (істинний), який «відлипає» або деактивує (робить хибним) логічний вимикач. Has Persistence option that allows the value of the logical switch to be preserved across power cycles or when switching away from and back to the model. </td></tr></tbody></table>
