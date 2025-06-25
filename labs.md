
---

<p>Хорошо, давайте разберем поставленную задачу. Вам нужно выполнить все задания из предоставленного пособия, а также дать подробные пошаговые инструкции. Для заданий, которые не могут быть выполнены непосредственно, необходимо предоставить подробные инструкции для их выполнения.</p>
<p>Я буду отвечать по частям, разбирая каждую лабораторную работу отдельно, следуя структуре предоставленного PDF-документа.</p>
<hr>
<p><strong>Общие рекомендации перед началом:</strong></p>
<ol>
<li><strong>Среда разработки:</strong> Вам потребуется текстовый редактор (например, Visual Studio Code, Sublime Text, Notepad++, или даже простой Блокнот) для написания HTML и JavaScript кода. Для просмотра результатов понадобится любой современный веб-браузер (Chrome, Firefox, Edge).</li>
<li><strong>Структура папок:</strong> Целесообразно создать отдельную папку для каждой лабораторной работы или даже для каждого задания внутри лабораторной работы, чтобы избежать путаницы с файлами (HTML, CSS, JS, изображения).</li>
<li><strong>Сохранение файлов:</strong> Сохраняйте HTML файлы с расширением <code>.html</code> (например, <code>index.html</code>), JavaScript файлы с расширением <code>.js</code> (например, <code>script.js</code>), а CSS файлы с расширением <code>.css</code> (например, <code>style.css</code>).</li>
<li><strong>Отладка:</strong> Внимательно прочитайте раздел “Отладка скрипта” на странице 4 пособия. Важно настроить браузер для отображения сообщений об ошибках JavaScript. В современных браузерах для отладки удобнее использовать встроенные Инструменты разработчика (обычно открываются по <code>F12</code>), вкладка “Console”.</li>
</ol>
<hr>
<p>Начнем с <strong>ЛАБОРАТОРНОЙ РАБОТЫ № 1: Введение в JavaScript</strong>.</p>
<hr>
<h3 id="лабораторная-работа-№-1-введение-в-javascript"><strong>ЛАБОРАТОРНАЯ РАБОТА № 1: Введение в JavaScript</strong></h3>
<p><strong>Цель:</strong> Изучить основы синтаксиса JavaScript, методы подключения скриптов к HTML-странице, ввод/вывод данных с использованием диалоговых окон <code>alert()</code>, <code>confirm()</code>, <code>prompt()</code>, а также метод <code>document.write()</code>.</p>
<p><strong>Общее описание:</strong></p>
<p>Пособие описывает четыре способа подключения JavaScript:</p>
<ol>
<li>В теговом контейне <code>&lt;BODY&gt;...&lt;/BODY&gt;</code>.</li>
<li>В теговом контейнере <code>&lt;HEAD&gt;...&lt;/HEAD&gt;</code> (для функций).</li>
<li>Во внешнем файле (<code>.js</code>).</li>
<li>Прямо в теге (как обработчик события).</li>
</ol>
<p>Для данной лабораторной работы будут использоваться в основном 1, 2 и 4 способы. Способ 3 (внешний файл) будет активно использоваться в следующих лабораториях.</p>
<p><strong>Примеры из пособия (стр. 8-14) и их выполнение:</strong></p>
<p><strong>Примеры 1, 2, 3 (стр. 8) - <code>alert()</code></strong></p>
<p>Эти примеры демонстрируют использование функции <code>alert()</code> для вывода сообщений. <code>alert()</code> - это простой способ показать пользователю информацию.</p>
<ul>
<li><code>alert(t)</code>: выводит значение переменной <code>t</code>.</li>
<li><code>alert(t + " text_2")</code>: конкатенация строк (объединение). JavaScript автоматически преобразует нестроковые операнды в строки при использовании оператора <code>+</code> со строками.</li>
<li><code>alert(t + "\n" + " text_2")</code>: использование символа новой строки <code>\n</code>.</li>
</ul>
<p><strong>Код для Пример 3 (содержит предыдущие идеи):</strong></p>
<p><strong>Файл: <code>lab1_alert.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Примеры alert()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Демонстрация alert()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Пример 1: Вывод значения переменной</span>
        <span class="token keyword">var</span> t1 <span class="token operator">=</span> <span class="token string">"текст_1"</span><span class="token punctuation">;</span>
        <span class="token function">alert</span><span class="token punctuation">(</span>t1<span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token comment">// Пример 2: Конкатенация строк</span>
        <span class="token keyword">var</span> t2_part1 <span class="token operator">=</span> <span class="token string">"Привет"</span><span class="token punctuation">;</span>
        <span class="token function">alert</span><span class="token punctuation">(</span>t2_part1 <span class="token operator">+</span> <span class="token string">" мир!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token comment">// Пример 3: Использование символа новой строки</span>
        <span class="token keyword">var</span> t3_part1 <span class="token operator">=</span> <span class="token string">"Это первая строка."</span><span class="token punctuation">;</span>
        <span class="token function">alert</span><span class="token punctuation">(</span>t3_part1 <span class="token operator">+</span> <span class="token string">"\n"</span> <span class="token operator">+</span> <span class="token string">"Это вторая строка."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab1_alert.html</code>.</li>
<li>Откройте файл <code>lab1_alert.html</code> в браузере.</li>
<li>Вы увидите последовательно три диалоговых окна <code>alert()</code>. Нажимайте “OK” для перехода к следующему.</li>
</ol>
<hr>
<p><strong>Пример (стр. 9) - <code>confirm()</code></strong></p>
<p>Этот пример демонстрирует использование <code>confirm()</code> для получения от пользователя ответа “Да” или “Нет” (<code>true</code> или <code>false</code>).</p>
<p><strong>Код для Примера <code>confirm()</code>:</strong></p>
<p><strong>Файл: <code>lab1_confirm.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример confirm()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Демонстрация confirm()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> result <span class="token operator">=</span> <span class="token function">confirm</span><span class="token punctuation">(</span><span class="token string">"Если 2*2=4 нажмите ОК, \nв противном случае нажмите Отмена"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">if</span> <span class="token punctuation">(</span>result<span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Молодец!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Учи таблицу умножения!!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab1_confirm.html</code>.</li>
<li>Откройте файл <code>lab1_confirm.html</code> в браузере.</li>
<li>Появится диалоговое окно <code>confirm()</code>. Нажмите “ОК” или “Отмена” и посмотрите соответствующий <code>alert()</code> ответ.</li>
</ol>
<hr>
<p><strong>Пример 1 (стр. 10) - <code>prompt()</code> и <code>parseInt()</code></strong></p>
<p>Этот пример показывает, как использовать <code>prompt()</code> для ввода данных пользователем и <code>parseInt()</code> для преобразования введенной строки в целое число.</p>
<p><strong>Код для Примера 1 <code>prompt()</code>:</strong></p>
<p><strong>Файл: <code>lab1_prompt1.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример prompt() с parseInt()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Демонстрация prompt()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> str <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"2*2="</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">if</span> <span class="token punctuation">(</span>str <span class="token operator">===</span> <span class="token string">"4"</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Используем === для строгого сравнения (значение и тип)</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Молодец!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Учи таблицу умножения!!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab1_prompt1.html</code>.</li>
<li>Откройте файл <code>lab1_prompt1.html</code> в браузере.</li>
<li>Введите “4” и нажмите “ОК”, затем перезагрузите страницу и введите другое число, чтобы увидеть разные результаты.</li>
</ol>
<hr>
<p><strong>Пример 2 (стр. 11) - Сумма двух чисел с <code>prompt()</code> и <code>parseInt()</code></strong></p>
<p>Этот пример более комплексен, он запрашивает два числа, преобразует их, суммирует и выводит результат. Также демонстрирует проблему с <code>NaN</code> (Not a Number), если введены нечисловые значения.</p>
<p><strong>Код для Примера 2 <code>prompt()</code>:</strong></p>
<p><strong>Файл: <code>lab1_prompt2.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Сумма двух чисел<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Вычисление суммы<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Запрос первого числа</span>
        <span class="token keyword">var</span> str1 <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"ВВЕДИТЕ ПЕРВОЕ ЧИСЛО:"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> x <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>str1<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Преобразование в целое число</span>

        <span class="token comment">// Запрос второго числа</span>
        <span class="token keyword">var</span> str2 <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"ВВЕДИТЕ ВТОРОЕ ЧИСЛО:"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> y <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>str2<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Преобразование в целое число</span>

        <span class="token comment">// Вычисление суммы</span>
        <span class="token keyword">var</span> s <span class="token operator">=</span> x <span class="token operator">+</span> y<span class="token punctuation">;</span>

        <span class="token comment">// Вывод результата</span>
        <span class="token comment">// Если x или y не преобразовались в число (были введены буквы), то s будет NaN</span>
        <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>s<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Введены нечисловые значения. Результат: "</span> <span class="token operator">+</span> s<span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Сумма равна "</span> <span class="token operator">+</span> s<span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab1_prompt2.html</code>.</li>
<li>Откройте файл <code>lab1_prompt2.html</code> в браузере.</li>
<li>Поэкспериментируйте:
<ul>
<li>Введите два числа (например, 23 и 74).</li>
<li>Введите число и буквы (например, 23 и “abc”).</li>
<li>Введите две строки из букв (например, “p” и “m”).</li>
</ul>
</li>
</ol>
<hr>
<p><strong>Пример 1 (стр. 12) - <code>document.write()</code></strong></p>
<p>Показывает, как динамически генерировать HTML-содержимое на странице. Важно: <code>document.write()</code> перезаписывает содержимое документа, если вызывается после полной загрузки страницы. В данных примерах она используется во время загрузки.</p>
<p><strong>Код для Примера 1 <code>document.write()</code>:</strong></p>
<p><strong>Файл: <code>lab1_document_write1.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример document.write()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Начало<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Динамическое добавление абзацев</span>
        document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;p&gt;абзац 1&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        document<span class="token punctuation">.</span><span class="token function">writeln</span><span class="token punctuation">(</span><span class="token string">"&lt;p&gt; абзац 2&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// writeln добавляет символ новой строки после строки, но это не влияет на HTML-рендеринг без CSS "white-space: pre"</span>
        document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;p&gt;абзац 3&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Конец<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab1_document_write1.html</code>.</li>
<li>Откройте файл <code>lab1_document_write1.html</code> в браузере.</li>
<li>Убедитесь, что абзацы отображаются между заголовками “Начало” и “Конец”.</li>
</ol>
<hr>
<p><strong>Пример 2 (стр. 14) - Цикл <code>for</code> и <code>document.write()</code></strong></p>
<p>Демонстрирует использование цикла <code>for</code> для динамического создания нескольких элементов.</p>
<p><strong>Код для Примера 2 с циклом <code>for</code>:</strong></p>
<p><strong>Файл: <code>lab1_loop1.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример цикла for<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Динамически сгенерированные строки<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> n <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">;</span>
        <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">var</span> i <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> i <span class="token operator">&lt;=</span> n<span class="token punctuation">;</span> i <span class="token operator">=</span> i <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;p&gt;Строка "</span> <span class="token operator">+</span> i <span class="token operator">+</span> <span class="token string">"&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab1_loop1.html</code>.</li>
<li>Откройте файл <code>lab1_loop1.html</code> в браузере.</li>
<li>Убедитесь, что отображаются три абзаца “Строка 1”, “Строка 2”, “Строка 3”.</li>
</ol>
<hr>
<p><strong>Пример 3 (стр. 14-15) - Шахматная доска с вложенными циклами и CSS</strong></p>
<p>Этот пример является более сложным и демонстрирует использование вложенных циклов для генерации динамической таблицы и стилизации ячеек с использованием CSS.</p>
<p><strong>Инструкции для создания файла CSS (1.css):</strong></p>
<p><strong>Файл: <code>1.css</code></strong></p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">table </span><span class="token punctuation">{</span>
    <span class="token property">border-collapse</span><span class="token punctuation">:</span> collapse<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token selector">td </span><span class="token punctuation">{</span>
    <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">50</span>px<span class="token punctuation">;</span>
    <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">50</span>px<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token selector"><span class="token class">.r1</span> </span><span class="token punctuation">{</span>
    <span class="token property">background-color</span><span class="token punctuation">:</span> red<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token selector"><span class="token class">.r2</span> </span><span class="token punctuation">{</span>
    <span class="token property">background-color</span><span class="token punctuation">:</span> blue<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<p><strong>Инструкции для создания файла HTML:</strong></p>
<p><strong>Файл: <code>lab1_chessboard.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Шахматная доска<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>link</span> <span class="token attr-name">rel</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>stylesheet<span class="token punctuation">"</span></span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/css<span class="token punctuation">"</span></span> <span class="token attr-name">href</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>1.css<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Шахматная доска 10x10<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> n <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span> <span class="token comment">// Размер доски n x n</span>
        <span class="token keyword">var</span> s<span class="token punctuation">;</span>      <span class="token comment">// строка для класса TD</span>

        document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;table&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">var</span> i <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> i <span class="token operator">&lt;=</span> n<span class="token punctuation">;</span> i <span class="token operator">=</span> i <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;tr&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Начало строки таблицы</span>

            <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">var</span> j <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> j <span class="token operator">&lt;=</span> n<span class="token punctuation">;</span> j <span class="token operator">=</span> j <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token comment">// Определяем класс ячейки в зависимости от четности суммы индексов i+j</span>
                <span class="token comment">// (i+j)%2 будет 0 для четных сумм и 1 для нечетных</span>
                <span class="token keyword">var</span> st <span class="token operator">=</span> <span class="token punctuation">(</span>i <span class="token operator">+</span> j<span class="token punctuation">)</span> <span class="token operator">%</span> <span class="token number">2</span><span class="token punctuation">;</span> 

                <span class="token keyword">if</span> <span class="token punctuation">(</span>st <span class="token operator">===</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    s <span class="token operator">=</span> <span class="token string">"class='r1'"</span><span class="token punctuation">;</span> <span class="token comment">// Красный для четных сумм</span>
                <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                    s <span class="token operator">=</span> <span class="token string">"class='r2'"</span><span class="token punctuation">;</span> <span class="token comment">// Синий для нечетных сумм</span>
                <span class="token punctuation">}</span>
                document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;td "</span> <span class="token operator">+</span> s <span class="token operator">+</span> <span class="token string">"&gt;&lt;/td&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Создаем ячейку с соответствующим классом</span>
            <span class="token punctuation">}</span>

            document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;/tr&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Конец строки таблицы</span>
        <span class="token punctuation">}</span>

        document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;/table&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token comment">// Примечание: document.write() используется здесь для демонстрации.</span>
        <span class="token comment">// В реальных проектах, особенно после загрузки DOM,</span>
        <span class="token comment">// предпочтительнее использовать методы DOM-манипуляций</span>
        <span class="token comment">// (например, createElement, appendChild) для создания элементов.</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Создайте новую папку, например, <code>lab1_chessboard</code>.</li>
<li>В этой папке создайте файл <code>1.css</code> и скопируйте в него CSS-код.</li>
<li>В этой же папке создайте файл <code>lab1_chessboard.html</code> и скопируйте в него HTML-код.</li>
<li>Откройте файл <code>lab1_chessboard.html</code> в браузере.</li>
<li>Вы должны увидеть шахматную доску 10x10 из синих и красных квадратов.</li>
</ol>
<hr>
<p><strong>Задание 1 (стр. 15-16) - Ввод ФИО и подтверждение</strong></p>
<p><strong>Задача Варианта 1:</strong> Ввести фамилию, имя и отчество, запросить подтверждение и вывести приветствие или сообщение об ошибке.</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Откройте текстовый редактор и сохраните пустой файл как <code>lab1_task1_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong> Добавьте базовый HTML-шаблон.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 1, Вариант 1<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Ввод ФИО и подтверждение<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Ваш JavaScript код будет здесь</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Используйте <code>prompt()</code> для ввода данных:</strong> Внутри <code>&lt;script&gt;</code> тега добавьте код для запроса фамилии, имени и отчества.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> lastName <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свою фамилию:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> firstName <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свое имя:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> middleName <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свое отчество:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Сформируйте полное ФИО:</strong> Объедините полученные значения в одну строку.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> fullName <span class="token operator">=</span> lastName <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> firstName <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> middleName<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Запросите подтверждение с <code>confirm()</code>:</strong> Задайте вопрос пользователю, является ли введенное ФИО верным.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> isCorrect <span class="token operator">=</span> <span class="token function">confirm</span><span class="token punctuation">(</span>fullName <span class="token operator">+</span> <span class="token string">"\nВсе верно?"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Выведите результат с <code>alert()</code> на основе подтверждения:</strong> Используйте оператор <code>if/else</code> для вывода соответствующего сообщения.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">if</span> <span class="token punctuation">(</span>isCorrect<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Молодец, "</span> <span class="token operator">+</span> fullName <span class="token operator">+</span> <span class="token string">"!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка в данных. Пожалуйста, попробуйте еще раз."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab1_task1_var1.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 1, Вариант 1<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Ввод ФИО и подтверждение<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> lastName <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свою фамилию:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> firstName <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свое имя:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> middleName <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свое отчество:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">var</span> fullName <span class="token operator">=</span> lastName <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> firstName <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> middleName<span class="token punctuation">;</span>

        <span class="token keyword">var</span> isCorrect <span class="token operator">=</span> <span class="token function">confirm</span><span class="token punctuation">(</span>fullName <span class="token operator">+</span> <span class="token string">"\nВсе верно?"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">if</span> <span class="token punctuation">(</span>isCorrect<span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Молодец, "</span> <span class="token operator">+</span> fullName <span class="token operator">+</span> <span class="token string">"!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка в данных. Пожалуйста, попробуйте еще раз."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab1_task1_var1.html</code> в браузере и протестируйте.</p>
</li>
</ol>
<hr>
<p><strong>Задание 2 (стр. 16-17) - Время через минуту</strong></p>
<p><strong>Задача Варианта 1:</strong> Ввести время (часы и минуты). Определить время, которое будет через минуту, используя вложенные операторы <code>if</code>. Возможны три случая (переход через час, переход через сутки, обычный).</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab1_task2_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 2, Вариант 1<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Время через минуту<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Ваш JavaScript код будет здесь</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Ввод часов и минут:</strong> Используйте <code>prompt()</code> и <code>parseInt()</code> для запроса текущих часов и минут.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> hoursStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите количество часов (0-23):"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> hours <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>hoursStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> minutesStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите количество минут (0-59):"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> minutes <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>minutesStr<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Валидация ввода:</strong> Убедитесь, что введенные значения являются числами и находятся в допустимом диапазоне. Если нет, выводите ошибку и завершайте.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>hours<span class="token punctuation">)</span> <span class="token operator">||</span> hours <span class="token operator">&lt;</span> <span class="token number">0</span> <span class="token operator">||</span> hours <span class="token operator">&gt;</span> <span class="token number">23</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>minutes<span class="token punctuation">)</span> <span class="token operator">||</span> minutes <span class="token operator">&lt;</span> <span class="token number">0</span> <span class="token operator">||</span> minutes <span class="token operator">&gt;</span> <span class="token number">59</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Некорректный ввод времени. Пожалуйста, введите числа в диапазоне."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
    <span class="token comment">// Логика вычисления времени будет здесь</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Вычисление времени через минуту:</strong></p>
<ul>
<li>Увеличьте минуты на 1.</li>
<li>Используйте вложенные <code>if</code> для обработки случаев:
<ul>
<li>Если минуты стали 60, сбросьте их в 0 и увеличьте часы.</li>
<li>Если часы стали 24, сбросьте их в 0 (переход через полночь).</li>
</ul>
</li>
</ul>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// (внутри блока else после валидации)</span>
minutes<span class="token operator">++</span><span class="token punctuation">;</span>

<span class="token keyword">if</span> <span class="token punctuation">(</span>minutes <span class="token operator">===</span> <span class="token number">60</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    minutes <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
    hours<span class="token operator">++</span><span class="token punctuation">;</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>hours <span class="token operator">===</span> <span class="token number">24</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
        hours <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Переход на следующий день</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Вывод результата:</strong> Используйте <code>alert()</code> для отображения нового времени. Форматируйте минуты с ведущим нулем, если они меньше 10.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// (после вычислений)</span>
<span class="token keyword">var</span> newMinutes <span class="token operator">=</span> <span class="token punctuation">(</span>minutes <span class="token operator">&lt;</span> <span class="token number">10</span> <span class="token operator">?</span> <span class="token string">"0"</span> <span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">)</span> <span class="token operator">+</span> minutes<span class="token punctuation">;</span> <span class="token comment">// Добавляем '0' для форматирования</span>
<span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Через минуту будет "</span> <span class="token operator">+</span> hours <span class="token operator">+</span> <span class="token string">" час и "</span> <span class="token operator">+</span> newMinutes <span class="token operator">+</span> <span class="token string">" мин"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab1_task2_var1.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 2, Вариант 1<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Время через минуту<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> hoursStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите количество часов (0-23):"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> hours <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>hoursStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">var</span> minutesStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите количество минут (0-59):"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> minutes <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>minutesStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>hours<span class="token punctuation">)</span> <span class="token operator">||</span> hours <span class="token operator">&lt;</span> <span class="token number">0</span> <span class="token operator">||</span> hours <span class="token operator">&gt;</span> <span class="token number">23</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>minutes<span class="token punctuation">)</span> <span class="token operator">||</span> minutes <span class="token operator">&lt;</span> <span class="token number">0</span> <span class="token operator">||</span> minutes <span class="token operator">&gt;</span> <span class="token number">59</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Некорректный ввод времени. Пожалуйста, введите числа в допустимом диапазоне."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
            minutes<span class="token operator">++</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>minutes <span class="token operator">===</span> <span class="token number">60</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                minutes <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
                hours<span class="token operator">++</span><span class="token punctuation">;</span>
                <span class="token keyword">if</span> <span class="token punctuation">(</span>hours <span class="token operator">===</span> <span class="token number">24</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    hours <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Переход на следующий день</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">}</span>
            <span class="token keyword">var</span> newMinutes <span class="token operator">=</span> <span class="token punctuation">(</span>minutes <span class="token operator">&lt;</span> <span class="token number">10</span> <span class="token operator">?</span> <span class="token string">"0"</span> <span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">)</span> <span class="token operator">+</span> minutes<span class="token punctuation">;</span> <span class="token comment">// Форматирование минут (добавление ведущего нуля)</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Через минуту будет "</span> <span class="token operator">+</span> hours <span class="token operator">+</span> <span class="token string">" час и "</span> <span class="token operator">+</span> newMinutes <span class="token operator">+</span> <span class="token string">" мин"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Проверьте различные варианты:</p>
<ul>
<li>14:35 -&gt; 14:36</li>
<li>14:59 -&gt; 15:00</li>
<li>23:59 -&gt; 0:00</li>
</ul>
</li>
</ol>
<hr>
<p><strong>Задание 3 (стр. 17) - Шахматная доска с другими цветами</strong></p>
<p><strong>Задача Варианта 1:</strong> Создать шахматную доску с другими цветами (синий и оранжевый или синий и розовый).</p>
<p>Это модификация Примера 3 (стр. 14-15).</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Скопируйте файлы:</strong> Скопируйте файлы <code>1.css</code> и <code>lab1_chessboard.html</code> из предыдущего Примера 3 в новую папку (например, <code>lab1_task3_var1</code>). Переименуйте <code>lab1_chessboard.html</code> в <code>lab1_task3_var1.html</code>.</p>
</li>
<li>
<p><strong>Измените цвета в CSS:</strong> Откройте <code>1.css</code> и поменяйте цвета.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">table </span><span class="token punctuation">{</span>
    <span class="token property">border-collapse</span><span class="token punctuation">:</span> collapse<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token selector">td </span><span class="token punctuation">{</span>
    <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">50</span>px<span class="token punctuation">;</span>
    <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">50</span>px<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token selector"><span class="token class">.r1</span> </span><span class="token punctuation">{</span>
    <span class="token property">background-color</span><span class="token punctuation">:</span> blue<span class="token punctuation">;</span> <span class="token comment">/* Изменен на синий */</span>
<span class="token punctuation">}</span>

<span class="token selector"><span class="token class">.r2</span> </span><span class="token punctuation">{</span>
    <span class="token property">background-color</span><span class="token punctuation">:</span> orange<span class="token punctuation">;</span> <span class="token comment">/* Изменен на оранжевый */</span>
<span class="token punctuation">}</span>
</code></pre>
<p>Или для розового:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector"><span class="token class">.r2</span> </span><span class="token punctuation">{</span>
    <span class="token property">background-color</span><span class="token punctuation">:</span> pink<span class="token punctuation">;</span> <span class="token comment">/* Изменен на розовый */</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Обновите HTML (необязательно, но желательно):</strong> В <code>lab1_task3_var1.html</code>, чтобы название отражало изменение, можете поменять заголовок <code>&lt;h1&gt;</code>:</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Шахматная доска 10x10 (Синий и Оранжевый)<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p>Остальной JavaScript-код в <code>&lt;script&gt;</code> <code>lab1_task3_var1.html</code> остается без изменений, так как он динамически назначает классы, а стили для этих классов определены в CSS.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab1_task3_var1.html</code> в браузере. Вы должны увидеть шахматную доску с новыми цветами.</p>
</li>
</ol>
<hr>
<p><strong>Задание 1 (стр. 17-18) - Ввод ФИО, пола, возраста, подтверждение</strong></p>
<p><strong>Задача Варианта 2:</strong> Ввести фамилию, пол и возраст, запросить подтверждение и вывести приветствие или сообщение об ошибке.</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab1_task1_var2.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 1, Вариант 2<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Ввод данных и подтверждение<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Ваш JavaScript код будет здесь</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Используйте <code>prompt()</code> для ввода данных:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> lastName <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свою фамилию:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> gender <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свой пол (м/ж):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> ageStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свой возраст:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> age <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>ageStr<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Валидация возраста:</strong> Убедитесь, что возраст является числом.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>age<span class="token punctuation">)</span> <span class="token operator">||</span> age <span class="token operator">&lt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Некорректный возраст."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
    <span class="token comment">// Продолжаем, если возраст корректен</span>
    <span class="token keyword">var</span> confirmationMessage <span class="token operator">=</span> <span class="token string">"ФИО: "</span> <span class="token operator">+</span> lastName <span class="token operator">+</span> 
                              <span class="token string">"\nПол: "</span> <span class="token operator">+</span> gender <span class="token operator">+</span> 
                              <span class="token string">"\nВозраст: "</span> <span class="token operator">+</span> age <span class="token operator">+</span> 
                              <span class="token string">"\nВсе верно?"</span><span class="token punctuation">;</span>
    
    <span class="token keyword">var</span> isConfirmed <span class="token operator">=</span> <span class="token function">confirm</span><span class="token punctuation">(</span>confirmationMessage<span class="token punctuation">)</span><span class="token punctuation">;</span>

    <span class="token keyword">if</span> <span class="token punctuation">(</span>isConfirmed<span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Молодец, "</span> <span class="token operator">+</span> lastName <span class="token operator">+</span> <span class="token string">"!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
        <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка в данных. Пожалуйста, попробуйте еще раз."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab1_task1_var2.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 1, Вариант 2<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Ввод данных и подтверждение<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> lastName <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свою фамилию:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> gender <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свой пол (м/ж):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> ageStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свой возраст:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> age <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>ageStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>age<span class="token punctuation">)</span> <span class="token operator">||</span> age <span class="token operator">&lt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Некорректный возраст. Возраст должен быть положительным числом."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> confirmationMessage <span class="token operator">=</span> <span class="token string">"ФИО: "</span> <span class="token operator">+</span> lastName <span class="token operator">+</span>
                                      <span class="token string">"\nПол: "</span> <span class="token operator">+</span> gender <span class="token operator">+</span>
                                      <span class="token string">"\nВозраст: "</span> <span class="token operator">+</span> age <span class="token operator">+</span>
                                      <span class="token string">"\nВсе верно?"</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> isConfirmed <span class="token operator">=</span> <span class="token function">confirm</span><span class="token punctuation">(</span>confirmationMessage<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>isConfirmed<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Молодец, "</span> <span class="token operator">+</span> lastName <span class="token operator">+</span> <span class="token string">"!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка в данных. Пожалуйста, попробуйте еще раз."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab1_task1_var2.html</code> в браузере и протестируйте.</p>
</li>
</ol>
<hr>
<p><strong>Задание 2 (стр. 18-19) - Калькулятор с арифметическими операциями</strong></p>
<p><strong>Задача Варианта 2:</strong> Дано два числа <code>x</code>, <code>y</code> и знак арифметической операции (<code>+</code>, <code>-</code>, <code>*</code>, <code>/</code>). Найти <code>x+y</code>, <code>x-y</code>, <code>x*y</code>, <code>x/y</code> в зависимости от введенного знака. В случае ошибки в знаке или деления на 0 вывести сообщение об ошибке.</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab1_task2_var2.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 2, Вариант 2 - Калькулятор<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Простой калькулятор<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Ваш JavaScript код будет здесь</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Ввод чисел и операции:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> num1Str <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите первое число:"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> num1 <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>num1Str<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Используем parseFloat для дробных чисел</span>

<span class="token keyword">var</span> num2Str <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите второе число:"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> num2 <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>num2Str<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> operator <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите знак операции (+, -, *, /):"</span><span class="token punctuation">,</span> <span class="token string">"+"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Валидация ввода чисел:</strong> Проверьте, что числа корректны.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>num1<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>num2<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Введены некорректные числа."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
    <span class="token comment">// Логика операций здесь</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Выполнение операции с использованием <code>if-else if-else</code>:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// (внутри блока else после валидации чисел)</span>
<span class="token keyword">var</span> result<span class="token punctuation">;</span>
<span class="token keyword">var</span> errorMessage <span class="token operator">=</span> <span class="token string">""</span><span class="token punctuation">;</span>

<span class="token keyword">if</span> <span class="token punctuation">(</span>operator <span class="token operator">===</span> <span class="token string">"+"</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    result <span class="token operator">=</span> num1 <span class="token operator">+</span> num2<span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>operator <span class="token operator">===</span> <span class="token string">"-"</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    result <span class="token operator">=</span> num1 <span class="token operator">-</span> num2<span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>operator <span class="token operator">===</span> <span class="token string">"*"</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    result <span class="token operator">=</span> num1 <span class="token operator">*</span> num2<span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>operator <span class="token operator">===</span> <span class="token string">"/"</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>num2 <span class="token operator">===</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
        errorMessage <span class="token operator">=</span> <span class="token string">"Ошибка: Деление на ноль невозможно."</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
        result <span class="token operator">=</span> num1 <span class="token operator">/</span> num2<span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
    errorMessage <span class="token operator">=</span> <span class="token string">"Ошибка: Неизвестная операция. Используйте +, -, *, или /."</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Вывод результата или ошибки:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// (после блока if-else if-else)</span>
<span class="token keyword">if</span> <span class="token punctuation">(</span>errorMessage<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span>errorMessage<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Результат: "</span> <span class="token operator">+</span> num1 <span class="token operator">+</span> operator <span class="token operator">+</span> num2 <span class="token operator">+</span> <span class="token string">" = "</span> <span class="token operator">+</span> result<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab1_task2_var2.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 2, Вариант 2 - Калькулятор<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Простой калькулятор<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> num1Str <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите первое число:"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> num1 <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>num1Str<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Используем parseFloat для поддержки дробных чисел</span>

        <span class="token keyword">var</span> num2Str <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите второе число:"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> num2 <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>num2Str<span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">var</span> operator <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите знак операции (+, -, *, /):"</span><span class="token punctuation">,</span> <span class="token string">"+"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>num1<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>num2<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Введены некорректные числа. Пожалуйста, введите числовые значения."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> result<span class="token punctuation">;</span>
            <span class="token keyword">var</span> errorMessage <span class="token operator">=</span> <span class="token string">""</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>operator <span class="token operator">===</span> <span class="token string">"+"</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                result <span class="token operator">=</span> num1 <span class="token operator">+</span> num2<span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>operator <span class="token operator">===</span> <span class="token string">"-"</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                result <span class="token operator">=</span> num1 <span class="token operator">-</span> num2<span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>operator <span class="token operator">===</span> <span class="token string">"*"</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                result <span class="token operator">=</span> num1 <span class="token operator">*</span> num2<span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>operator <span class="token operator">===</span> <span class="token string">"/"</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token keyword">if</span> <span class="token punctuation">(</span>num2 <span class="token operator">===</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    errorMessage <span class="token operator">=</span> <span class="token string">"Ошибка: Деление на ноль невозможно."</span><span class="token punctuation">;</span>
                <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                    result <span class="token operator">=</span> num1 <span class="token operator">/</span> num2<span class="token punctuation">;</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                errorMessage <span class="token operator">=</span> <span class="token string">"Ошибка: Неизвестная операция. Используйте +, -, *, или /."</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>errorMessage<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span>errorMessage<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Результат: "</span> <span class="token operator">+</span> num1 <span class="token operator">+</span> operator <span class="token operator">+</span> num2 <span class="token operator">+</span> <span class="token string">" = "</span> <span class="token operator">+</span> result<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Проверьте различные сценарии:</p>
<ul>
<li>45, 15, +</li>
<li>45, 15, /</li>
<li>10, 0, /</li>
<li>“abc”, 5, +</li>
<li>10, 5, “x”</li>
</ul>
</li>
</ol>
<hr>
<p><strong>Задание 3 (стр. 19) - Шахматная доска с другими цветами</strong></p>
<p><strong>Задача Варианта 2:</strong> Создать шахматную доску с другими цветами (синий и светло-синий).</p>
<p>Это еще одна модификация Примера 3 (стр. 14-15).</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Скопируйте файлы:</strong> Скопируйте файлы <code>1.css</code> и <code>lab1_chessboard.html</code> из Примера 3 (или из Задания 3 Варианта 1) в новую папку (например, <code>lab1_task3_var2</code>). Переименуйте <code>lab1_chessboard.html</code> в <code>lab1_task3_var2.html</code>.</p>
</li>
<li>
<p><strong>Измените цвета в CSS:</strong> Откройте <code>1.css</code> и поменяйте цвета.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">table </span><span class="token punctuation">{</span>
    <span class="token property">border-collapse</span><span class="token punctuation">:</span> collapse<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token selector">td </span><span class="token punctuation">{</span>
    <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">50</span>px<span class="token punctuation">;</span>
    <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">50</span>px<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token selector"><span class="token class">.r1</span> </span><span class="token punctuation">{</span>
    <span class="token property">background-color</span><span class="token punctuation">:</span> blue<span class="token punctuation">;</span> <span class="token comment">/* Синий */</span>
<span class="token punctuation">}</span>

<span class="token selector"><span class="token class">.r2</span> </span><span class="token punctuation">{</span>
    <span class="token property">background-color</span><span class="token punctuation">:</span> lightblue<span class="token punctuation">;</span> <span class="token comment">/* Светло-синий */</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Обновите HTML (желательно):</strong> В <code>lab1_task3_var2.html</code>, можете поменять заголовок <code>&lt;h1&gt;</code>:</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Шахматная доска 10x10 (Синий и Светло-синий)<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p>Остальной JavaScript-код остается без изменений.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab1_task3_var2.html</code> в браузере. Вы должны увидеть шахматную доску с новыми цветами.</p>
</li>
</ol>
<hr>
<p>Это завершает <strong>ЛАБОРАТОРНУЮ РАБОТУ № 1</strong>.<br>
Я предоставил готовые решения для всех примеров и заданий, а также подробные пошаговые инструкции для их выполнения.**</p>
<p>Отлично! Переходим к <strong>ЛАБОРАТОРНОЙ РАБОТЕ № 2: События и функции</strong>.</p>
<hr>
<h3 id="лабораторная-работа-№-2-события-и-функции"><strong>ЛАБОРАТОРНАЯ РАБОТА № 2: События и функции</strong></h3>
<p><strong>Цель:</strong> Изучить механизм обработки событий в JavaScript, создание и использование функций, а также их взаимодействие с HTML-элементами.</p>
<p><strong>Общее описание:</strong></p>
<p>В этой лабораторной работе мы будем работать с:</p>
<ul>
<li><strong>Событиями:</strong> <code>onLoad</code> (загрузка страницы), <code>onClick</code> (клик мышью).</li>
<li><strong>Функциями:</strong> Описание, вызов, передача параметров, возвращаемые значения.</li>
<li><strong>Подключением обработчиков:</strong> Непосредственно в теге HTML.</li>
</ul>
<hr>
<p><strong>Примеры из пособия (стр. 20-22) и их выполнение:</strong></p>
<p><strong>Пример (стр. 20) - Событие <code>onLoad</code></strong></p>
<p>Демонстрирует, как выполнить JavaScript-код после полной загрузки страницы с использованием атрибута <code>onLoad</code> в теге <code>&lt;body&gt;</code>.</p>
<p><strong>Код для Примера <code>onLoad</code>:</strong></p>
<p><strong>Файл: <code>lab2_onload.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример onLoad<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span> <span class="token attr-name">onLoad</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>alert(<span class="token punctuation">'</span>Документ загружен<span class="token punctuation">'</span>);<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Обработчик события onLoad<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Вызывается метод alert() после загрузки страницы<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab2_onload.html</code> (или <code>События.html</code>, как в пособии).</li>
<li>Откройте файл <code>lab2_onload.html</code> в браузере.</li>
<li>Вы должны увидеть диалоговое окно <code>alert()</code> с сообщением “Документ загружен” сразу после того, как страница полностью загрузится.</li>
</ol>
<hr>
<p><strong>Пример (стр. 21) - Событие <code>onClick</code></strong></p>
<p>Демонстрирует, как привязать JavaScript-код к событию клика по кнопке с использованием атрибута <code>onClick</code>.</p>
<p><strong>Код для Примера <code>onClick</code>:</strong></p>
<p><strong>Файл: <code>lab2_onclick.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример onClick<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Обработчик события onClick<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Нажми меня нежно<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>alert(<span class="token punctuation">'</span>Спасибо!!<span class="token punctuation">'</span>);<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab2_onclick.html</code> (или <code>События2.html</code>, как в пособии).</li>
<li>Откройте файл <code>lab2_onclick.html</code> в браузере.</li>
<li>Нажмите кнопку “Нажми меня нежно”. Вы должны увидеть диалоговое окно <code>alert()</code> с сообщением “Спасибо!!”.</li>
</ol>
<hr>
<p><strong>Пример 1 (стр. 22) - Функция без параметров и с глобальным вводом/выводом</strong></p>
<p>Демонстрирует создание функции (<code>chet</code>), которая не принимает параметров и не возвращает значения, но использует глобальные <code>prompt()</code> для ввода и <code>alert()</code> для вывода. Функция вызывается по <code>onClick</code>.</p>
<p><strong>Код для Примера 1 с функцией:</strong></p>
<p><strong>Файл: <code>lab2_function1.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример функции без параметров<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Определение функции chet</span>
        <span class="token keyword">function</span> <span class="token function">chet</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> str1 <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"ВВЕДИТЕ ПЕРВОЕ ЧИСЛО:"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> x <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>str1<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> str2 <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"ВВЕДИТЕ ВТОРОЕ ЧИСЛО:"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> y <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>str2<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> s <span class="token operator">=</span> x <span class="token operator">+</span> y<span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>s<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Введены некорректные числа. Результат: "</span> <span class="token operator">+</span> s<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Сумма равна "</span> <span class="token operator">+</span> s<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Использование функций<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Посчитаем!!<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>chet();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab2_function1.html</code> (или <code>Функция_Событие.html</code>, как в пособии).</li>
<li>Откройте файл <code>lab2_function1.html</code> в браузере.</li>
<li>Нажмите кнопку “Посчитаем!!”. Введите числа в <code>prompt()</code> и увидите результат в <code>alert()</code>. Проверьте ввод некорректных данных.</li>
</ol>
<hr>
<p><strong>Пример 2 (стр. 23) - Функция с параметрами</strong></p>
<p>Демонстрирует создание функции (<code>chet</code>), которая принимает два параметра. Ввод чисел происходит НЕ внутри функции, а до её вызова.</p>
<p><strong>Код для Примера 2 с функцией:</strong></p>
<p><strong>Файл: <code>lab2_function2.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример функции с параметрами<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Определение функции chet, принимающей два строковых параметра</span>
        <span class="token keyword">function</span> <span class="token function">chet</span><span class="token punctuation">(</span>st1<span class="token punctuation">,</span> st2<span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> x <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>st1<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Преобразуем первый параметр в число</span>
            <span class="token keyword">var</span> y <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>st2<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Преобразуем второй параметр в число</span>
            <span class="token keyword">var</span> s <span class="token operator">=</span> x <span class="token operator">+</span> y<span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>s<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Введены некорректные числа. Результат: "</span> <span class="token operator">+</span> s<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Сумма равна "</span> <span class="token operator">+</span> s<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Использование функций с параметрами<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Запрос чисел до вызова функции</span>
        <span class="token keyword">var</span> str1 <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"ВВЕДИТЕ ПЕРВОЕ ЧИСЛО:"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> str2 <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"ВВЕДИТЕ ВТОРОЕ ЧИСЛО:"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
    <span class="token comment">&lt;!-- Кнопка, которая вызывает функцию chet и передает ей полученные значения str1 и str2 --&gt;</span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Найдем сумму<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>chet(str1, str2);<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab2_function2.html</code> (или <code>Функция_Событие2.html</code>, как в пособии).</li>
<li>Откройте файл <code>lab2_function2.html</code> в браузере.</li>
<li>Сначала появятся два <code>prompt()</code> для ввода чисел, затем появится страница с кнопкой. Нажмите кнопку “Найдем сумму”, чтобы увидеть результат.</li>
</ol>
<hr>
<p><strong>Задание (стр. 23) - Оформление Задания 2 из Лабораторной работы 1 как функция</strong></p>
<p><strong>Задача:</strong> Оформить задание 2 из Лабораторной работы 1 (Время через минуту) в виде функции и вызвать эту функцию по нажатию кнопки.</p>
<p>Мы уже выполнили Задание 2 из Лабораторной работы 1. Теперь нужно инкапсулировать эту логику в функцию.</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab2_task_time.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура с функцией:</strong><br>
Вся логика из <code>lab1_task2_var1.html</code> будет перемещена в функцию.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание: Время через минуту (функция)<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Определение функции calculateNextMinute</span>
        <span class="token keyword">function</span> <span class="token function">calculateNextMinute</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> hoursStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите количество часов (0-23):"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> hours <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>hoursStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> minutesStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите количество минут (0-59):"</span><span class="token punctuation">,</span> <span class="token string">"0"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> minutes <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>minutesStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>hours<span class="token punctuation">)</span> <span class="token operator">||</span> hours <span class="token operator">&lt;</span> <span class="token number">0</span> <span class="token operator">||</span> hours <span class="token operator">&gt;</span> <span class="token number">23</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>minutes<span class="token punctuation">)</span> <span class="token operator">||</span> minutes <span class="token operator">&lt;</span> <span class="token number">0</span> <span class="token operator">||</span> minutes <span class="token operator">&gt;</span> <span class="token number">59</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Некорректный ввод времени. Пожалуйста, введите числа в допустимом диапазоне."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                minutes<span class="token operator">++</span><span class="token punctuation">;</span>

                <span class="token keyword">if</span> <span class="token punctuation">(</span>minutes <span class="token operator">===</span> <span class="token number">60</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    minutes <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
                    hours<span class="token operator">++</span><span class="token punctuation">;</span>
                    <span class="token keyword">if</span> <span class="token punctuation">(</span>hours <span class="token operator">===</span> <span class="token number">24</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                        hours <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Переход на следующий день (00:00 следующего дня)</span>
                    <span class="token punctuation">}</span>
                <span class="token punctuation">}</span>
                <span class="token keyword">var</span> newMinutes <span class="token operator">=</span> <span class="token punctuation">(</span>minutes <span class="token operator">&lt;</span> <span class="token number">10</span> <span class="token operator">?</span> <span class="token string">"0"</span> <span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">)</span> <span class="token operator">+</span> minutes<span class="token punctuation">;</span> <span class="token comment">// Форматирование минут (добавление ведущего нуля)</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Через минуту будет "</span> <span class="token operator">+</span> hours <span class="token operator">+</span> <span class="token string">" час и "</span> <span class="token operator">+</span> newMinutes <span class="token operator">+</span> <span class="token string">" мин"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Время через минуту<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Вычислить время через минуту<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>calculateNextMinute();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Заключительная проверка:</strong> Проверьте, что функция <code>calculateNextMinute()</code> определена в <code>&lt;script&gt;</code> в <code>&lt;head&gt;</code> (или в <code>&lt;body&gt;</code> до использования кнопки), и что кнопка вызывает эту функцию по <code>onClick</code>.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab2_task_time.html</code> в браузере. Нажмите кнопку и проверьте работу калькулятора времени.</p>
</li>
</ol>
<hr>
<p>Это завершает <strong>ЛАБОРАТОРНУЮ РАБОТУ № 2</strong>.</p>
<p>Отлично! Переходим к <strong>ЛАБОРАТОРНОЙ РАБОТЕ № 3: Встроенные объекты</strong>.</p>
<hr>
<h3 id="лабораторная-работа-№-3-встроенные-объекты"><strong>ЛАБОРАТОРНАЯ РАБОТА № 3: Встроенные объекты</strong></h3>
<p><strong>Цель:</strong> Изучить использование встроенных объектов JavaScript, в частности <code>Math</code> и <code>Date</code>, для выполнения математических вычислений и работы с датами и временем. Также будет введено понятие объекта <code>Array</code> и фундаментальное для DOM-манипуляций понятие <code>document.getElementById()</code>.</p>
<p><strong>Общее описание:</strong></p>
<ul>
<li><strong>Объект <code>Math</code>:</strong> Предоставляет математические константы и функции (например, <code>Math.PI</code>, <code>Math.sqrt()</code>, <code>Math.floor()</code>).</li>
<li><strong>Объект <code>Date</code>:</strong> Позволяет создавать, манипулировать и форматировать даты и время.</li>
<li><strong>Объект <code>Array</code>:</strong> Используется для создания и работы с массивами данных.</li>
<li><strong><code>document.getElementById()</code>:</strong> Ключевой метод для получения HTML-элемента по его <code>id</code>.</li>
<li><strong><code>element.value</code>:</strong> Доступ к значению HTML-элемента формы.</li>
</ul>
<hr>
<p><strong>Примеры из пособия (стр. 24-30) и их выполнение:</strong></p>
<p><strong>Пример (стр. 24) - <code>Math.floor()</code></strong></p>
<p>Демонстрирует использование метода <code>Math.floor()</code> для округления числа вниз.</p>
<p><strong>Код для Примера <code>Math.floor()</code>:</strong></p>
<p><strong>Файл: <code>lab3_math_floor.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример Math.floor()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Демонстрация Math.floor()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> d1 <span class="token operator">=</span> <span class="token number">45.6</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> d2 <span class="token operator">=</span> Math<span class="token punctuation">.</span><span class="token function">floor</span><span class="token punctuation">(</span>d1<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Округляет 45.6 до 45</span>

        <span class="token function">alert</span><span class="token punctuation">(</span>d2<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Выведет 45</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab3_math_floor.html</code>.</li>
<li>Откройте файл <code>lab3_math_floor.html</code> в браузере.</li>
<li>Вы увидите <code>alert()</code> с числом 45.</li>
</ol>
<hr>
<p><strong>Пример 1 (стр. 26) - <code>Date</code> и <code>getYear()</code></strong></p>
<p>Демонстрирует создание объекта <code>Date</code> для текущей даты и времени, а также использование метода <code>getYear()</code> для получения года.</p>
<p><strong>Код для Примера 1 <code>Date</code>:</strong></p>
<p><strong>Файл: <code>lab3_date_getyear.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример Date и getYear()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Демонстрация Date и getYear()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> today <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Создаем объект Date с текущей датой и временем</span>
        <span class="token keyword">var</span> god <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Получаем год. Внимание: getYear() устарел и может возвращать год - 1900.</span>
                                <span class="token comment">// Для корректного года в современных браузерах используйте getFullYear().</span>
                                <span class="token comment">// Но для соответствия пособию, используем getYear().</span>
        <span class="token function">alert</span><span class="token punctuation">(</span>god<span class="token punctuation">)</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Примечание:</strong> В современных браузерах <code>getYear()</code> устарел и возвращает год минус 1900 для годов до 2000, и полный год для 2000 и выше. Правильнее использовать <code>getFullYear()</code>. Для целей лабораторной, следуем пособию.</p>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab3_date_getyear.html</code>.</li>
<li>Откройте файл <code>lab3_date_getyear.html</code> в браузере.</li>
<li>В <code>alert()</code> вы увидите текущий год.</li>
</ol>
<hr>
<p><strong>Пример 2 (стр. 26) - <code>Date</code> и <code>getDay()</code></strong></p>
<p>Демонстрирует создание объекта <code>Date</code> для конкретной даты и использование метода <code>getDay()</code> для получения дня недели (0 для воскресенья, 1 для понедельника и т.д.).</p>
<p><strong>Код для Примера 2 <code>Date</code>:</strong></p>
<p><strong>Файл: <code>lab3_date_getday.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример Date и getDay()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Демонстрация Date и getDay()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Создаем объект Date для 21 мая 1958 года. Месяцы в JavaScript начинаются с 0 (апрель = 4).</span>
        <span class="token keyword">var</span> dr <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token number">1958</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">,</span> <span class="token number">21</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> dn <span class="token operator">=</span> dr<span class="token punctuation">.</span><span class="token function">getDay</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Получаем день недели (0=воскресенье, 1=понедельник, ..., 6=суббота)</span>
        <span class="token function">alert</span><span class="token punctuation">(</span>dn<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 21 мая 1958 года был средой, что соответствует 3</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab3_date_getday.html</code>.</li>
<li>Откройте файл <code>lab3_date_getday.html</code> в браузере.</li>
<li>Вы увидите <code>alert()</code> с числом 3.</li>
</ol>
<hr>
<p><strong>Пример 3 (стр. 27) - <code>Array</code> и <code>getDay()</code></strong></p>
<p>Комбинирует <code>Date</code> и <code>Array</code> для вывода названия дня недели по его номеру.</p>
<p><strong>Код для Примера 3 <code>Array</code>:</strong></p>
<p><strong>Файл: <code>lab3_array_dayname.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример Array и getDay()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Демонстрация Array и getDay()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Создаем объект Date для 21 мая 1958 года</span>
        <span class="token keyword">var</span> dr <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token number">1958</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">,</span> <span class="token number">21</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> dn <span class="token operator">=</span> dr<span class="token punctuation">.</span><span class="token function">getDay</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Получаем номер дня недели (0=воскресенье, 1=понедельник, ...)</span>

        <span class="token comment">// Создаем массив с названиями дней недели</span>
        <span class="token keyword">var</span> dayn <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Array</span><span class="token punctuation">(</span><span class="token string">'воскресенье'</span><span class="token punctuation">,</span> <span class="token string">'понедельник'</span><span class="token punctuation">,</span> <span class="token string">'вторник'</span><span class="token punctuation">,</span> <span class="token string">'среда'</span><span class="token punctuation">,</span> <span class="token string">'четверг'</span><span class="token punctuation">,</span> <span class="token string">'пятница'</span><span class="token punctuation">,</span> <span class="token string">'суббота'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token comment">// Используем номер дня недели как индекс для получения названия из массива</span>
        <span class="token function">alert</span><span class="token punctuation">(</span>dayn<span class="token punctuation">[</span>dn<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// dayn[3] -&gt; 'среда'</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab3_array_dayname.html</code>.</li>
<li>Откройте файл <code>lab3_array_dayname.html</code> в браузере.</li>
<li>Вы увидите <code>alert()</code> с названием “среда”.</li>
</ol>
<hr>
<p><strong>Пример 4 (стр. 28) - <code>document.getElementById()</code> и <code>element.value</code></strong></p>
<p>Демонстрирует, как получить доступ к HTML-элементу (в данном случае, текстовому полю) по его <code>id</code>, и как изменить его содержимое через свойство <code>value</code>.</p>
<p><strong>Код для Примера 4 <code>getElementById()</code>:</strong></p>
<p><strong>Файл: <code>lab3_getelementbyid.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Пример document.getElementById()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">gd</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> today <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Текущая дата и время</span>
            <span class="token comment">// Для корректного года в 21-м веке используем getFullYear(), не getYear()</span>
            <span class="token keyword">var</span> god <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Получаем полный год (например, 2023)</span>

            <span class="token comment">// Получаем ссылку на текстовое поле по его id 'f1'</span>
            <span class="token keyword">var</span> p1 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'f1'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Присваиваем значение года свойству 'value' текстового поля</span>
            p1<span class="token punctuation">.</span>value <span class="token operator">=</span> god<span class="token punctuation">;</span> <span class="token comment">// Текстовое поле будет отображать текущий год</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token comment">&lt;!-- Функция gd() будет вызвана, когда страница полностью загрузится --&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span> <span class="token attr-name">onLoad</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>gd();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Демонстрация document.getElementById()<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>f1<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Текущий год:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>f1<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>f1<span class="token punctuation">"</span></span> <span class="token attr-name">size</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>8<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab3_getelementbyid.html</code>.</li>
<li>Откройте файл <code>lab3_getelementbyid.html</code> в браузере.</li>
<li>После загрузки страницы, текстовое поле должно автоматически заполниться текущим годом.</li>
</ol>
<hr>
<p><strong>Пример 5 (стр. 29) - Количество дней с начала года</strong></p>
<p>Вычисляет, сколько дней прошло с начала текущего года, используя объекты <code>Date</code> и <code>Math.floor()</code>.</p>
<p><strong>Код для Примера 5:</strong></p>
<p><strong>Файл: <code>lab3_days_since_year_start.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Дни с начала года<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Дни с начала года<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Переменная today имеет значение текущее время и дата</span>
        <span class="token keyword">var</span> today <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token comment">// Переменная y - текущий год (используем getFullYear() для корректности)</span>
        <span class="token keyword">var</span> y <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 

        <span class="token comment">// Переменная yearBegin имеет значение начала текущего года (1 января)</span>
        <span class="token comment">// Месяцы в Date начинаются с 0 (0 = январь)</span>
        <span class="token keyword">var</span> yearBegin <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span>y<span class="token punctuation">,</span> <span class="token number">0</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 

        <span class="token comment">// Переменная d - количество миллисекунд от начала эпохи (1 января 1970г) до текущей даты</span>
        <span class="token comment">// и от начала года. Разница дает миллисекунды прошедшие в этом году.</span>
        <span class="token keyword">var</span> d_milliseconds <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">-</span> yearBegin<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token comment">// Переведем d_milliseconds в дни. В сутках 86,400,000 миллисекунд.</span>
        <span class="token keyword">var</span> days <span class="token operator">=</span> d_milliseconds <span class="token operator">/</span> <span class="token punctuation">(</span><span class="token number">1000</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">24</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 1000ms * 60s * 60min * 24h</span>

        <span class="token comment">// Прибавим 1, иначе 1 января будет нулевым днем</span>
        days <span class="token operator">=</span> days <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// 1 января - первый день</span>

        <span class="token comment">// Отбросим дробную часть</span>
        days <span class="token operator">=</span> Math<span class="token punctuation">.</span><span class="token function">floor</span><span class="token punctuation">(</span>days<span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token comment">// Печать результата</span>
        document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;h2&gt;Сегодня "</span> <span class="token operator">+</span> days <span class="token operator">+</span> <span class="token string">" день с начала года&lt;/h2&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        
        <span class="token comment">// Дополнительно: можно вывести в console для проверки</span>
        console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Текущая дата (мс): "</span><span class="token operator">+</span> today<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Начало года (мс): "</span><span class="token operator">+</span> yearBegin<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Разница (мс): "</span><span class="token operator">+</span> d_milliseconds<span class="token punctuation">)</span><span class="token punctuation">;</span>
        console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Дни (float): "</span><span class="token operator">+</span> <span class="token punctuation">(</span>d_milliseconds <span class="token operator">/</span> <span class="token punctuation">(</span><span class="token number">1000</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">24</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Итого дней: "</span><span class="token operator">+</span> days<span class="token punctuation">)</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab3_days_since_year_start.html</code>.</li>
<li>Откройте файл <code>lab3_days_since_year_start.html</code> в браузере.</li>
<li>На странице должно отобразиться количество дней, прошедших с начала года.</li>
</ol>
<hr>
<p><strong>Пример 6 (стр. 30) - Вычисление площади круга</strong></p>
<p>Вычисляет площадь круга на основе радиуса, введенного в текстовое поле. Используется <code>Math.PI</code> и <code>Math.pow()</code> (или просто <code>r*r</code>). Результат выводится в <code>alert()</code>.</p>
<p><strong>Код для Примера 6:</strong></p>
<p><strong>Файл: <code>lab3_circle_area.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Вычисление площади круга<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">h1 </span><span class="token punctuation">{</span><span class="token property">color</span><span class="token punctuation">:</span>red<span class="token punctuation">;</span><span class="token property">text-align</span><span class="token punctuation">:</span>center<span class="token punctuation">;</span><span class="token punctuation">}</span>
        <span class="token selector">body </span><span class="token punctuation">{</span><span class="token property">background-color</span><span class="token punctuation">:</span>PaleGreen<span class="token punctuation">;</span> <span class="token property">font-weight</span><span class="token punctuation">:</span>bold<span class="token punctuation">;</span><span class="token punctuation">}</span>
        <span class="token selector">input </span><span class="token punctuation">{</span><span class="token property">font-weight</span><span class="token punctuation">:</span>bold<span class="token punctuation">;</span><span class="token punctuation">}</span>
        <span class="token selector">form </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token punctuation">}</span> <span class="token comment">/* Центрируем форму */</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">sqr</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Функция для вычисления площади</span>
            <span class="token comment">// Получаем ссылку на текстовое поле с id 't'</span>
            <span class="token keyword">var</span> p <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'t'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Получаем значение из текстового поля и преобразуем его в число (радиус)</span>
            <span class="token keyword">var</span> r <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>p<span class="token punctuation">.</span>value<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Проверяем, является ли радиус корректным числом</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>r<span class="token punctuation">)</span> <span class="token operator">||</span> r <span class="token operator">&lt;</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Пожалуйста, введите корректный радиус (число &gt; 0)."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span> <span class="token comment">// Выходим из функции</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Вычисляем площадь круга: PI * r^2</span>
            <span class="token comment">// var s = Math.PI * Math.pow(r, 2); // Использование Math.pow()</span>
            <span class="token keyword">var</span> s <span class="token operator">=</span> Math<span class="token punctuation">.</span>PI <span class="token operator">*</span> r <span class="token operator">*</span> r<span class="token punctuation">;</span> <span class="token comment">// Более простой способ для r^2</span>

            <span class="token comment">// Выводим результат</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Площадь круга: "</span> <span class="token operator">+</span> s<span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Площадь круга<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>hr</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>t<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Радиус:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>6<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>t<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>t<span class="token punctuation">"</span></span> <span class="token attr-name">size</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>5<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Площадь<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>sqr();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>hr</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab3_circle_area.html</code>.</li>
<li>Откройте файл <code>lab3_circle_area.html</code> в браузере.</li>
<li>Введите радиус (например, 6) и нажмите кнопку “Площадь”. Проверьте также ввод некорректных значений.</li>
</ol>
<hr>
<p><strong>Задание 1 (стр. 31) - Вариант 1 (Дата загрузки страницы)</strong></p>
<p><strong>Задача:</strong> Создать HTML-страницу, которая при загрузке выводит на страницу текущий день недели, число, месяц и год. Для месяцев и дней недели организовать массивы.</p>
<p><strong>Решено:</strong> Комбинация <code>Date</code> + <code>Array</code> + <code>document.write()</code></p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab3_task1_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 1, Вариант 1 - Текущая дата<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Сегодня<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Ваш JavaScript код будет здесь</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Получение текущей даты и ее компонентов:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> today <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> dayOfWeekNum <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getDay</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>    <span class="token comment">// 0=вс, 1=пн...</span>
<span class="token keyword">var</span> dayOfMonth <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getDate</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>     <span class="token comment">// День месяца</span>
<span class="token keyword">var</span> monthNum <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getMonth</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>      <span class="token comment">// 0=янв, 1=фев...</span>
<span class="token keyword">var</span> year <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>       <span class="token comment">// Полный год</span>
</code></pre>
</li>
<li>
<p><strong>Создание массивов для дней недели и месяцев:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> days <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">'воскресенье'</span><span class="token punctuation">,</span> <span class="token string">'понедельник'</span><span class="token punctuation">,</span> <span class="token string">'вторник'</span><span class="token punctuation">,</span> <span class="token string">'среда'</span><span class="token punctuation">,</span> <span class="token string">'четверг'</span><span class="token punctuation">,</span> <span class="token string">'пятница'</span><span class="token punctuation">,</span> <span class="token string">'суббота'</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> months <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">'января'</span><span class="token punctuation">,</span> <span class="token string">'февраля'</span><span class="token punctuation">,</span> <span class="token string">'марта'</span><span class="token punctuation">,</span> <span class="token string">'апреля'</span><span class="token punctuation">,</span> <span class="token string">'мая'</span><span class="token punctuation">,</span> <span class="token string">'июня'</span><span class="token punctuation">,</span> <span class="token string">'июля'</span><span class="token punctuation">,</span> <span class="token string">'августа'</span><span class="token punctuation">,</span> <span class="token string">'сентября'</span><span class="token punctuation">,</span> <span class="token string">'октября'</span><span class="token punctuation">,</span> <span class="token string">'ноября'</span><span class="token punctuation">,</span> <span class="token string">'декабря'</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Получение строковых представлений:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> dayOfWeekName <span class="token operator">=</span> days<span class="token punctuation">[</span>dayOfWeekNum<span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> monthName <span class="token operator">=</span> months<span class="token punctuation">[</span>monthNum<span class="token punctuation">]</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Динамический вывод на страницу:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript">document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;h2&gt;"</span> <span class="token operator">+</span> dayOfMonth <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> monthName <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> year <span class="token operator">+</span> <span class="token string">" года, "</span> <span class="token operator">+</span> dayOfWeekName <span class="token operator">+</span> <span class="token string">"&lt;/h2&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab3_task1_var1.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 1, Вариант 1 - Текущая дата<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span> <span class="token attr-name">onLoad</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>displayDate();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Сегодня<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Можно обернуть в функцию и вызвать по onLoad</span>
        <span class="token keyword">function</span> <span class="token function">displayDate</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> today <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> dayOfWeekNum <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getDay</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>    <span class="token comment">// 0=вс, 1=пн...</span>
            <span class="token keyword">var</span> dayOfMonth <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getDate</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>     <span class="token comment">// День месяца (1-31)</span>
            <span class="token keyword">var</span> monthNum <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getMonth</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>      <span class="token comment">// 0=янв, 1=фев...</span>
            <span class="token keyword">var</span> year <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>       <span class="token comment">// Полный год (например, 2023)</span>

            <span class="token keyword">var</span> days <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">'воскресенье'</span><span class="token punctuation">,</span> <span class="token string">'понедельник'</span><span class="token punctuation">,</span> <span class="token string">'вторник'</span><span class="token punctuation">,</span> <span class="token string">'среда'</span><span class="token punctuation">,</span> <span class="token string">'четверг'</span><span class="token punctuation">,</span> <span class="token string">'пятница'</span><span class="token punctuation">,</span> <span class="token string">'суббота'</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> months <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">'января'</span><span class="token punctuation">,</span> <span class="token string">'февраля'</span><span class="token punctuation">,</span> <span class="token string">'марта'</span><span class="token punctuation">,</span> <span class="token string">'апреля'</span><span class="token punctuation">,</span> <span class="token string">'мая'</span><span class="token punctuation">,</span> <span class="token string">'июня'</span><span class="token punctuation">,</span> <span class="token string">'июля'</span><span class="token punctuation">,</span> <span class="token string">'августа'</span><span class="token punctuation">,</span> <span class="token string">'сентября'</span><span class="token punctuation">,</span> <span class="token string">'октября'</span><span class="token punctuation">,</span> <span class="token string">'ноября'</span><span class="token punctuation">,</span> <span class="token string">'декабря'</span><span class="token punctuation">]</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> dayOfWeekName <span class="token operator">=</span> days<span class="token punctuation">[</span>dayOfWeekNum<span class="token punctuation">]</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> monthName <span class="token operator">=</span> months<span class="token punctuation">[</span>monthNum<span class="token punctuation">]</span><span class="token punctuation">;</span>

            document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;h2&gt;"</span> <span class="token operator">+</span> dayOfMonth <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> monthName <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> year <span class="token operator">+</span> <span class="token string">" года, "</span> <span class="token operator">+</span> dayOfWeekName <span class="token operator">+</span> <span class="token string">"&lt;/h2&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token function">displayDate</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Вызываем функцию непосредственно при загрузке скрипта</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab3_task1_var1.html</code> в браузере. Вы должны увидеть текущую дату и день недели.</p>
</li>
</ol>
<hr>
<p><strong>Задание 2 (стр. 31) - Вариант 1 (Дни, прожитые вами)</strong></p>
<p><strong>Задача:</strong> Создать HTML-страницу, которая при загрузке запрашивает дату вашего рождения и выводит количество дней, которые вы прожили, в текстовое поле формы.</p>
<p><strong>Решено:</strong> <code>Date</code> + <code>prompt()</code> + <code>getElementById()</code> + <code>element.value</code> + <code>Math.floor()</code></p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab3_task2_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура с текстовым полем:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 2, Вариант 1 - Количество прожитых дней<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Ваш JavaScript код будет здесь</span>
        <span class="token keyword">function</span> <span class="token function">calculateDays</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Логика будет здесь</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span> <span class="token attr-name">onLoad</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>calculateDays();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Сколько дней прожито<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysLived<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Я прожил всего<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysLived<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysLived<span class="token punctuation">"</span></span> <span class="token attr-name">size</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>10<span class="token punctuation">"</span></span> <span class="token attr-name">readonly</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span><span class="token punctuation">&gt;</span></span>дней<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Ввод даты рождения и ее валидация:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Внутри calculateDays()</span>
<span class="token keyword">var</span> birthYearStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите год вашего рождения (например, 1990):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> birthMonthStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите номер месяца рождения (1-12):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> birthDayStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите день рождения (1-31):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> birthYear <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthYearStr<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> birthMonth <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthMonthStr<span class="token punctuation">)</span> <span class="token operator">-</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Месяцы в Date с 0</span>
<span class="token keyword">var</span> birthDay <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthDayStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Проверка на корректность ввода</span>
<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>birthYear<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>birthMonth<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>birthDay<span class="token punctuation">)</span> <span class="token operator">||</span>
    birthYear <span class="token operator">&lt;</span> <span class="token number">1900</span> <span class="token operator">||</span> birthYear <span class="token operator">&gt;</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">||</span>
    birthMonth <span class="token operator">&lt;</span> <span class="token number">0</span> <span class="token operator">||</span> birthMonth <span class="token operator">&gt;</span> <span class="token number">11</span> <span class="token operator">||</span>
    birthDay <span class="token operator">&lt;</span> <span class="token number">1</span> <span class="token operator">||</span> birthDay <span class="token operator">&gt;</span> <span class="token number">31</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Некорректная дата рождения."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">return</span><span class="token punctuation">;</span> <span class="token comment">// Прекращаем выполнение функции</span>
<span class="token punctuation">}</span>

<span class="token keyword">var</span> birthDate <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span>birthYear<span class="token punctuation">,</span> birthMonth<span class="token punctuation">,</span> birthDay<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> today <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Вычисление разницы в миллисекундах и перевод в дни:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Продолжение calculateDays()</span>
<span class="token keyword">var</span> diffMilliseconds <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">-</span> birthDate<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> daysLived <span class="token operator">=</span> diffMilliseconds <span class="token operator">/</span> <span class="token punctuation">(</span><span class="token number">1000</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">24</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Миллисекунды в одном дне</span>

daysLived <span class="token operator">=</span> Math<span class="token punctuation">.</span><span class="token function">floor</span><span class="token punctuation">(</span>daysLived<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Округляем до целых дней</span>
</code></pre>
</li>
<li>
<p><strong>Отображение результата в текстовом поле:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Продолжение calculateDays()</span>
<span class="token keyword">var</span> inputField <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'daysLived'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
inputField<span class="token punctuation">.</span>value <span class="token operator">=</span> daysLived<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab3_task2_var1.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 2, Вариант 1 - Количество прожитых дней<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">calculateDays</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> birthYearStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите год вашего рождения (например, 1990):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> birthMonthStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите номер месяца рождения (1-12):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> birthDayStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите день рождения (1-31):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> birthYear <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthYearStr<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> birthMonth <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthMonthStr<span class="token punctuation">)</span> <span class="token operator">-</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Месяцы в Date начинаются с 0 (январь = 0)</span>
            <span class="token keyword">var</span> birthDay <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthDayStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Расширенная проверка на корректность ввода даты</span>
            <span class="token keyword">var</span> isValidDate <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>birthYear<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>birthMonth<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>birthDay<span class="token punctuation">)</span> <span class="token operator">||</span> birthYear <span class="token operator">&lt;</span> <span class="token number">1900</span> <span class="token operator">||</span> birthYear <span class="token operator">&gt;</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                isValidDate <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token keyword">var</span> testDate <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span>birthYear<span class="token punctuation">,</span> birthMonth<span class="token punctuation">,</span> birthDay<span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token comment">// Проверяем, что Date объект не изменил введенные значения (т.е. дата корректна: 31 февраля станет 2 марта)</span>
                <span class="token keyword">if</span> <span class="token punctuation">(</span>testDate<span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">!==</span> birthYear <span class="token operator">||</span> testDate<span class="token punctuation">.</span><span class="token function">getMonth</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">!==</span> birthMonth <span class="token operator">||</span> testDate<span class="token punctuation">.</span><span class="token function">getDate</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">!==</span> birthDay<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    isValidDate <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">}</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>isValidDate<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Некорректная дата рождения. Пожалуйста, введите корректные числовые значения."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span> <span class="token comment">// Прекращаем выполнение функции</span>
            <span class="token punctuation">}</span>
            
            <span class="token keyword">var</span> birthDate <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span>birthYear<span class="token punctuation">,</span> birthMonth<span class="token punctuation">,</span> birthDay<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> today <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Вычисляем разницу в миллисекундах</span>
            <span class="token keyword">var</span> diffMilliseconds <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">-</span> birthDate<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Переводим миллисекунды в дни. Запас с Math.floor() на неполный день.</span>
            <span class="token keyword">var</span> daysLived <span class="token operator">=</span> Math<span class="token punctuation">.</span><span class="token function">floor</span><span class="token punctuation">(</span>diffMilliseconds <span class="token operator">/</span> <span class="token punctuation">(</span><span class="token number">1000</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">24</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 1000ms * 60s * 60min * 24h</span>

            <span class="token keyword">var</span> inputField <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'daysLived'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            inputField<span class="token punctuation">.</span>value <span class="token operator">=</span> daysLived<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span> <span class="token attr-name">onLoad</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>calculateDays();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Сколько дней прожито<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysLived<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Я прожил всего<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysLived<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysLived<span class="token punctuation">"</span></span> <span class="token attr-name">size</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>10<span class="token punctuation">"</span></span> <span class="token attr-name">readonly</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span><span class="token punctuation">&gt;</span></span>дней<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab3_task2_var1.html</code> в браузере. Введите вашу дату рождения и увидите количество прожитых дней. Протестируйте некорректный ввод (например, “февраль”, “32”, “2050”).</p>
</li>
</ol>
<hr>
<p><strong>Задание 3 (стр. 31) - Вариант 1 (Расстояние от точки до начала координат)</strong></p>
<p><strong>Задача:</strong> Ввести координаты точки (x, y) в поля формы и определить расстояние от этой точки до начала координат (0,0). Расстояние должно вычисляться по нажатию кнопки.</p>
<p><strong>Решено:</strong> <code>getElementById()</code> + <code>element.value</code> + <code>parseFloat()</code> + <code>Math.sqrt()</code> + <code>Math.pow()</code></p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab3_task3_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура с формой и кнопкой:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 3, Вариант 1 - Расстояние до начала координат<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#e0f2f7</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.container</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#c8e6f1</span><span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#a7d9ed</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">400</span>px<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">label, input, button </span><span class="token punctuation">{</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token function">calc</span><span class="token punctuation">(</span><span class="token number">100%</span> - <span class="token number">22</span>px<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">button </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#4CAF50</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">button<span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#45a049</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">calculateDistance</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Логика будет здесь</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Расстояние от точки до начала координат<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span><span class="token punctuation">&gt;</span></span>Введите координаты точки:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>coordX<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>X:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>coordX<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>3<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>coordY<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Y:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>coordY<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>4<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>calculateDistance();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Вычислить расстояние<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>distance<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Расстояние:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>distance<span class="token punctuation">"</span></span> <span class="token attr-name">readonly</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Получение координат, валидация и вычисление:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Внутри calculateDistance() function</span>
<span class="token keyword">var</span> xStr <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'coordX'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
<span class="token keyword">var</span> yStr <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'coordY'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>

<span class="token keyword">var</span> x <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>xStr<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> y <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>yStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>x<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>y<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Пожалуйста, введите числовые координаты X и Y."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'distance'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">""</span><span class="token punctuation">;</span> <span class="token comment">// Очищаем поле вывода</span>
    <span class="token keyword">return</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token comment">// Расстояние d = sqrt(x^2 + y^2)</span>
<span class="token keyword">var</span> dist <span class="token operator">=</span> Math<span class="token punctuation">.</span><span class="token function">sqrt</span><span class="token punctuation">(</span>Math<span class="token punctuation">.</span><span class="token function">pow</span><span class="token punctuation">(</span>x<span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span> <span class="token operator">+</span> Math<span class="token punctuation">.</span><span class="token function">pow</span><span class="token punctuation">(</span>y<span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token comment">// Или Math.sqrt(x*x + y*y);</span>

document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'distance'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> dist<span class="token punctuation">.</span><span class="token function">toFixed</span><span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Выводим с 2 знаками после запятой</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab3_task3_var1.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 3, Вариант 1 - Расстояние до начала координат<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#e0f2f7</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.container</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#c8e6f1</span><span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#a7d9ed</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">400</span>px<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">label, input, button </span><span class="token punctuation">{</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token function">calc</span><span class="token punctuation">(</span><span class="token number">100%</span> - <span class="token number">22</span>px<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">button </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#4CAF50</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">button<span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#45a049</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">calculateDistance</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> xStr <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'coordX'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
            <span class="token keyword">var</span> yStr <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'coordY'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>

            <span class="token keyword">var</span> x <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>xStr<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> y <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>yStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>x<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>y<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Пожалуйста, введите числовые координаты X и Y."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'distance'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">""</span><span class="token punctuation">;</span> <span class="token comment">// Очищаем поле вывода</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Расстояние от точки (x,y) до (0,0) вычисляется по формуле: sqrt(x^2 + y^2)</span>
            <span class="token keyword">var</span> dist <span class="token operator">=</span> Math<span class="token punctuation">.</span><span class="token function">sqrt</span><span class="token punctuation">(</span>Math<span class="token punctuation">.</span><span class="token function">pow</span><span class="token punctuation">(</span>x<span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span> <span class="token operator">+</span> Math<span class="token punctuation">.</span><span class="token function">pow</span><span class="token punctuation">(</span>y<span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Выводим результат в текстовое поле 'distance', округляем до двух знаков после запятой</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'distance'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> dist<span class="token punctuation">.</span><span class="token function">toFixed</span><span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Расстояние от точки до начала координат<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span><span class="token punctuation">&gt;</span></span>Введите координаты точки:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>coordX<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>X:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>coordX<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>3<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>coordY<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Y:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>coordY<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>4<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>calculateDistance();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Вычислить расстояние<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>distance<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Расстояние:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>distance<span class="token punctuation">"</span></span> <span class="token attr-name">readonly</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab3_task3_var1.html</code> в браузере. Введиет 3 и 4, нажмите кнопку - должно быть 5.00. Проверьте некорректный ввод.</p>
</li>
</ol>
<hr>
<p><strong>Задание 1 (стр. 32) - Вариант 2 (Дата рождения и день недели)</strong></p>
<p><strong>Задача:</strong> Создать HTML-страницу, которая при загрузке запрашивает дату вашего рождения и выводит на страницу день недели, число, месяц и год этой даты. Для месяцев и дней недели организовать массивы.</p>
<p><strong>Решено:</strong> <code>Date</code> + <code>prompt()</code> + <code>Array</code> + <code>document.write()</code></p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab3_task1_var2.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 1, Вариант 2 - Дата рождения и день недели<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>День рождения<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Ваш JavaScript код будет здесь</span>
        <span class="token keyword">function</span> <span class="token function">showBirthDateDetails</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Логика будет здесь</span>
        <span class="token punctuation">}</span>
        <span class="token function">showBirthDateDetails</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Вызываем при загрузке</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Ввод даты рождения и валидация:</strong> Аналогично Заданию 2 Варианта 1, но теперь нам нужна именно дата для отображения, а не просто количество дней.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Внутри showBirthDateDetails()</span>
<span class="token keyword">var</span> birthYearStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите год вашего рождения (например, 1990):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> birthMonthStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите номер месяца рождения (1-12):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> birthDayStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите день рождения (1-31):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> birthYear <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthYearStr<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> birthMonth <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthMonthStr<span class="token punctuation">)</span> <span class="token operator">-</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Месяцы в Date с 0</span>
<span class="token keyword">var</span> birthDay <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthDayStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> birthDate <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span>birthYear<span class="token punctuation">,</span> birthMonth<span class="token punctuation">,</span> birthDay<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Расширенная проверка на корректность введенной даты</span>
<span class="token keyword">var</span> isValidDate <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span>
<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>birthYear<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>birthMonth<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>birthDay<span class="token punctuation">)</span> <span class="token operator">||</span> birthYear <span class="token operator">&lt;</span> <span class="token number">1900</span> <span class="token operator">||</span> birthYear <span class="token operator">&gt;</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    isValidDate <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
    <span class="token keyword">var</span> testDate <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span>birthYear<span class="token punctuation">,</span> birthMonth<span class="token punctuation">,</span> birthDay<span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>testDate<span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">!==</span> birthYear <span class="token operator">||</span> testDate<span class="token punctuation">.</span><span class="token function">getMonth</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">!==</span> birthMonth <span class="token operator">||</span> testDate<span class="token punctuation">.</span><span class="token function">getDate</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">!==</span> birthDay<span class="token punctuation">)</span> <span class="token punctuation">{</span>
        isValidDate <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>

<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>isValidDate<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;p style='color:red;'&gt;Ошибка: Некорректная дата рождения. Страница не может быть сформирована.&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">return</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Массивы для дней недели и месяцев:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Продолжение showBirthDateDetails()</span>
<span class="token keyword">var</span> days <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">'воскресенье'</span><span class="token punctuation">,</span> <span class="token string">'понедельник'</span><span class="token punctuation">,</span> <span class="token string">'вторник'</span><span class="token punctuation">,</span> <span class="token string">'среда'</span><span class="token punctuation">,</span> <span class="token string">'четверг'</span><span class="token punctuation">,</span> <span class="token string">'пятница'</span><span class="token punctuation">,</span> <span class="token string">'суббота'</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> months <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">'января'</span><span class="token punctuation">,</span> <span class="token string">'февраля'</span><span class="token punctuation">,</span> <span class="token string">'марта'</span><span class="token punctuation">,</span> <span class="token string">'апреля'</span><span class="token punctuation">,</span> <span class="token string">'мая'</span><span class="token punctuation">,</span> <span class="token string">'июня'</span><span class="token punctuation">,</span> <span class="token string">'июля'</span><span class="token punctuation">,</span> <span class="token string">'августа'</span><span class="token punctuation">,</span> <span class="token string">'сентября'</span><span class="token punctuation">,</span> <span class="token string">'октября'</span><span class="token punctuation">,</span> <span class="token string">'ноября'</span><span class="token punctuation">,</span> <span class="token string">'декабря'</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Получение данных для вывода:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Продолжение showBirthDateDetails()</span>
<span class="token keyword">var</span> dayOfWeekName <span class="token operator">=</span> days<span class="token punctuation">[</span>birthDate<span class="token punctuation">.</span><span class="token function">getDay</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> monthName <span class="token operator">=</span> months<span class="token punctuation">[</span>birthDate<span class="token punctuation">.</span><span class="token function">getMonth</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> displayDay <span class="token operator">=</span> birthDate<span class="token punctuation">.</span><span class="token function">getDate</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> displayYear <span class="token operator">=</span> birthDate<span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Динамический вывод на страницу:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Продолжение showBirthDateDetails()</span>
document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;h2&gt;Я родился "</span> <span class="token operator">+</span> displayDay <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> monthName <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> displayYear <span class="token operator">+</span> <span class="token string">" года в "</span> <span class="token operator">+</span> dayOfWeekName <span class="token operator">+</span> <span class="token string">"&lt;/h2&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab3_task1_var2.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 1, Вариант 2 - Дата рождения и день недели<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>День рождения<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">showBirthDateDetails</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> birthYearStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите год вашего рождения (например, 1990):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> birthMonthStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите номер месяца рождения (1-12):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> birthDayStr <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите день рождения (1-31):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> birthYear <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthYearStr<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> birthMonth <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthMonthStr<span class="token punctuation">)</span> <span class="token operator">-</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Месяцы в Date начинаются с 0</span>
            <span class="token keyword">var</span> birthDay <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span>birthDayStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Создаем Date объект для введенной даты</span>
            <span class="token keyword">var</span> birthDate <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span>birthYear<span class="token punctuation">,</span> birthMonth<span class="token punctuation">,</span> birthDay<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Валидация: проверяем, что введенные значения действительно формируют ту дату, которую ожидали</span>
            <span class="token comment">// (например, Date(2023, 1, 30) для 30 февраля станет 2 марта)</span>
            <span class="token keyword">var</span> isValidDate <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>birthYear<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>birthMonth<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>birthDay<span class="token punctuation">)</span> <span class="token operator">||</span> birthYear <span class="token operator">&lt;</span> <span class="token number">1</span> <span class="token operator">||</span> birthYear <span class="token operator">&gt;</span> <span class="token number">9999</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Простой диапазон</span>
                isValidDate <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token comment">// Проверяем, что введенная дата не изменилась после создания Date объекта</span>
                <span class="token keyword">if</span> <span class="token punctuation">(</span>birthDate<span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">!==</span> birthYear <span class="token operator">||</span> birthDate<span class="token punctuation">.</span><span class="token function">getMonth</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">!==</span> birthMonth <span class="token operator">||</span> birthDate<span class="token punctuation">.</span><span class="token function">getDate</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">!==</span> birthDay<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    isValidDate <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">}</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>isValidDate<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;p style='color:red;'&gt;Ошибка: Некорректная дата рождения. Введите, пожалуйста, правильные числовые значения.&lt;/p&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span> <span class="token comment">// Прекращаем выполнение</span>
            <span class="token punctuation">}</span>

            <span class="token keyword">var</span> days <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">'воскресенье'</span><span class="token punctuation">,</span> <span class="token string">'понедельник'</span><span class="token punctuation">,</span> <span class="token string">'вторник'</span><span class="token punctuation">,</span> <span class="token string">'среда'</span><span class="token punctuation">,</span> <span class="token string">'четверг'</span><span class="token punctuation">,</span> <span class="token string">'пятница'</span><span class="token punctuation">,</span> <span class="token string">'суббота'</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> months <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">'января'</span><span class="token punctuation">,</span> <span class="token string">'февраля'</span><span class="token punctuation">,</span> <span class="token string">'марта'</span><span class="token punctuation">,</span> <span class="token string">'апреля'</span><span class="token punctuation">,</span> <span class="token string">'мая'</span><span class="token punctuation">,</span> <span class="token string">'июня'</span><span class="token punctuation">,</span> <span class="token string">'июля'</span><span class="token punctuation">,</span> <span class="token string">'августа'</span><span class="token punctuation">,</span> <span class="token string">'сентября'</span><span class="token punctuation">,</span> <span class="token string">'октября'</span><span class="token punctuation">,</span> <span class="token string">'ноября'</span><span class="token punctuation">,</span> <span class="token string">'декабря'</span><span class="token punctuation">]</span><span class="token punctuation">;</span>

            <span class="token comment">// Получаем день недели и название месяца из сформированной даты</span>
            <span class="token keyword">var</span> dayOfWeekName <span class="token operator">=</span> days<span class="token punctuation">[</span>birthDate<span class="token punctuation">.</span><span class="token function">getDay</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> monthName <span class="token operator">=</span> months<span class="token punctuation">[</span>birthDate<span class="token punctuation">.</span><span class="token function">getMonth</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> displayDay <span class="token operator">=</span> birthDate<span class="token punctuation">.</span><span class="token function">getDate</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> displayYear <span class="token operator">=</span> birthDate<span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;h2&gt;Я родился "</span> <span class="token operator">+</span> displayDay <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> monthName <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> displayYear <span class="token operator">+</span> <span class="token string">" года в "</span> <span class="token operator">+</span> dayOfWeekName <span class="token operator">+</span> <span class="token string">"&lt;/h2&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token function">showBirthDateDetails</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab3_task1_var2.html</code> в браузере. Введиет дату рождения и увидите результат.</p>
</li>
</ol>
<hr>
<p><strong>Задание 2 (стр. 32) - Вариант 2 (Дни до каникул)</strong></p>
<p><strong>Задача:</strong> Создать HTML-страницу, которая при загрузке выводит в текстовое поле формы, сколько дней осталось до каникул.</p>
<p><strong>Решено:</strong> <code>Date</code> + <code>getElementById()</code> + <code>element.value</code> + <code>Math.ceil()</code> (здесь <code>ceil</code>, потому что оставшиеся дни - это “достичь”, а не “прожить”).</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab3_task2_var2.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура с текстовым полем:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 2, Вариант 2 - Дни до каникул<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">calculateDaysUntilVacation</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Логика будет здесь</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span> <span class="token attr-name">onLoad</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>calculateDaysUntilVacation();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Дни до каникул<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysUntil<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>До каникул осталось<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysUntil<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysUntil<span class="token punctuation">"</span></span> <span class="token attr-name">size</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>5<span class="token punctuation">"</span></span> <span class="token attr-name">readonly</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span><span class="token punctuation">&gt;</span></span>дней<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Определение даты каникул и вычисление разницы:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Внутри calculateDaysUntilVacation()</span>
<span class="token keyword">var</span> today <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> currentYear <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Определим дату каникул. Например, 1 июня текущего года.</span>
<span class="token comment">// Если 1 июня уже прошло, то каникулы в следующем году.</span>
<span class="token keyword">var</span> vacationDate <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span>currentYear<span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Месяц 5 = Июнь</span>

<span class="token comment">// Если дата каникул в текущем году уже прошла, пересчитываем на следующий год</span>
<span class="token keyword">if</span> <span class="token punctuation">(</span>today <span class="token operator">&gt;</span> vacationDate<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    vacationDate <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span>currentYear <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Каникулы в следующем году</span>
<span class="token punctuation">}</span>

<span class="token keyword">var</span> diffMilliseconds <span class="token operator">=</span> vacationDate<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">-</span> today<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> daysUntil <span class="token operator">=</span> Math<span class="token punctuation">.</span><span class="token function">ceil</span><span class="token punctuation">(</span>diffMilliseconds <span class="token operator">/</span> <span class="token punctuation">(</span><span class="token number">1000</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">24</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Округляем вверх</span>
</code></pre>
</li>
<li>
<p><strong>Отображение результата:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Продолжение calculateDaysUntilVacation()</span>
<span class="token keyword">var</span> inputField <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'daysUntil'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
inputField<span class="token punctuation">.</span>value <span class="token operator">=</span> daysUntil<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab3_task2_var2.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 2, Вариант 2 - Дни до каникул<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">calculateDaysUntilVacation</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> today <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> currentYear <span class="token operator">=</span> today<span class="token punctuation">.</span><span class="token function">getFullYear</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Определим дату начала каникул (например, 1 июня)</span>
            <span class="token comment">// Можно сделать интерактивным через prompt</span>
            <span class="token keyword">var</span> vacationMonth <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">;</span> <span class="token comment">// Июнь (0-11)</span>
            <span class="token keyword">var</span> vacationDay <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> vacationDate <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span>currentYear<span class="token punctuation">,</span> vacationMonth<span class="token punctuation">,</span> vacationDay<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Если каникулы этого года уже прошли, то считаем до каникул следующего года</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>today<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">&gt;</span> vacationDate<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                vacationDate <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span>currentYear <span class="token operator">+</span> <span class="token number">1</span><span class="token punctuation">,</span> vacationMonth<span class="token punctuation">,</span> vacationDay<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Вычисляем разницу в миллисекундах</span>
            <span class="token keyword">var</span> diffMilliseconds <span class="token operator">=</span> vacationDate<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">-</span> today<span class="token punctuation">.</span><span class="token function">getTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Переводим миллисекунды в дни, округляем вверх, так как если осталось даже 0.1 дня, это считается "еще один день"</span>
            <span class="token keyword">var</span> daysUntil <span class="token operator">=</span> Math<span class="token punctuation">.</span><span class="token function">ceil</span><span class="token punctuation">(</span>diffMilliseconds <span class="token operator">/</span> <span class="token punctuation">(</span><span class="token number">1000</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">60</span> <span class="token operator">*</span> <span class="token number">24</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> inputField <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'daysUntil'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            inputField<span class="token punctuation">.</span>value <span class="token operator">=</span> daysUntil<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span> <span class="token attr-name">onLoad</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>calculateDaysUntilVacation();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Дни до каникул<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysUntil<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>До каникул осталось<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysUntil<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>daysUntil<span class="token punctuation">"</span></span> <span class="token attr-name">size</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>5<span class="token punctuation">"</span></span> <span class="token attr-name">readonly</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span><span class="token punctuation">&gt;</span></span>дней<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab3_task2_var2.html</code> в браузере. Поле должно заполниться количеством дней.</p>
</li>
</ol>
<hr>
<p><strong>Задание 3 (стр. 32) - Вариант 2 (Площадь прямоугольника)</strong></p>
<p><strong>Задача:</strong> Ввести длину и ширину прямоугольника в поля формы и определить площадь этого прямоугольника. Площадь должна вычисляться по нажатию кнопки.</p>
<p><strong>Решено:</strong> <code>getElementById()</code> + <code>element.value</code> + <code>parseFloat()</code></p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab3_task3_var2.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура с формой и кнопкой:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 3, Вариант 2 - Площадь прямоугольника<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f8ff</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.container</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#e0f2f7</span><span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#d0e8ef</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">400</span>px<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">label, input </span><span class="token punctuation">{</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> inline-block<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">45%</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">button </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#007bff</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">button<span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#0056b3</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.result-label</span>, <span class="token class">.result-input</span> </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">calculateArea</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Логика будет здесь</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Площадь прямоугольника<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>length<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Длина:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>length<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>10<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>width<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Ширина:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>width<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>8<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>calculateArea();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Вычислить площадь<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>area<span class="token punctuation">"</span></span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>result-label<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Площадь:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>area<span class="token punctuation">"</span></span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>result-input<span class="token punctuation">"</span></span> <span class="token attr-name">readonly</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Получение значений, валидация и вычисление:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Внутри calculateArea() function</span>
<span class="token keyword">var</span> lengthStr <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'length'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
<span class="token keyword">var</span> widthStr <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'width'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>

<span class="token keyword">var</span> length <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>lengthStr<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> width <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>widthStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>length<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>width<span class="token punctuation">)</span> <span class="token operator">||</span> length <span class="token operator">&lt;=</span> <span class="token number">0</span> <span class="token operator">||</span> width <span class="token operator">&lt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Пожалуйста, введите положительные числовые значения для длины и ширины."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'area'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">""</span><span class="token punctuation">;</span> <span class="token comment">// Очищаем поле вывода</span>
    <span class="token keyword">return</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">var</span> area <span class="token operator">=</span> length <span class="token operator">*</span> width<span class="token punctuation">;</span>

document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'area'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> area<span class="token punctuation">.</span><span class="token function">toFixed</span><span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Выводим с 2 знаками после запятой</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab3_task3_var2.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Задание 3, Вариант 2 - Площадь прямоугольника<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f8ff</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.container</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#e0f2f7</span><span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#d0e8ef</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">400</span>px<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">label, input </span><span class="token punctuation">{</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> inline-block<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">45%</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">button </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#007bff</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">button<span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#0056b3</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.result-label</span>, <span class="token class">.result-input</span> </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">calculateArea</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> lengthStr <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'length'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
            <span class="token keyword">var</span> widthStr <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'width'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>

            <span class="token keyword">var</span> length <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>lengthStr<span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> width <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span>widthStr<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>length<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>width<span class="token punctuation">)</span> <span class="token operator">||</span> length <span class="token operator">&lt;=</span> <span class="token number">0</span> <span class="token operator">||</span> width <span class="token operator">&lt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Пожалуйста, введите положительные числовые значения для длины и ширины."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'area'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">""</span><span class="token punctuation">;</span> <span class="token comment">// Очищаем поле вывода</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token keyword">var</span> area <span class="token operator">=</span> length <span class="token operator">*</span> width<span class="token punctuation">;</span>

            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'area'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> area<span class="token punctuation">.</span><span class="token function">toFixed</span><span class="token punctuation">(</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Площадь прямоугольника<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>length<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Длина:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>length<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>10<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>width<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Ширина:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>width<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>8<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>calculateArea();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Вычислить площадь<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>area<span class="token punctuation">"</span></span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>result-label<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Площадь:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>area<span class="token punctuation">"</span></span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>result-input<span class="token punctuation">"</span></span> <span class="token attr-name">readonly</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab3_task3_var2.html</code> в браузере. Введите длину и ширину, нажмите кнопку.</p>
</li>
</ol>
<hr>
<p>Это завершает <strong>ЛАБОРАТОРНУЮ РАБОТУ № 3</strong>.</p>
<p>Отлично! Переходим к <strong>ЛАБОРАТОРНОЙ РАБОТЕ № 4: Объект Window</strong>.</p>
<hr>
<h3 id="лабораторная-работа-№-4-объект-window"><strong>ЛАБОРАТОРНАЯ РАБОТА № 4: Объект Window</strong></h3>
<p><strong>Цель:</strong> Изучить объект <code>window</code> и его основные методы, особенно <code>window.open()</code> и <code>window.close()</code>, для управления окнами/вкладками браузера. Также будут рассмотрены диалоговые окна (которые являются методами <code>window</code>) и основы динамического формирования HTML в новом окне.</p>
<p><strong>Общее описание:</strong></p>
<p>Объект <code>window</code> представляет собой открытое окно браузера и является глобальным объектом в JavaScript на стороне клиента. Все глобальные переменные и функции автоматически становятся свойствами объекта <code>window</code>.</p>
<p>Основные методы, которые будут рассмотрены:</p>
<ul>
<li><code>window.alert()</code>, <code>window.confirm()</code>, <code>window.prompt()</code>: уже знакомые диалоговые окна являются методами <code>window</code>.</li>
<li><code>window.open(url, windowName, features)</code>: Открывает новое окно/вкладку.
<ul>
<li><code>url</code>: URL документа для загрузки.</li>
<li><code>windowName</code>: Имя окна (произвольная строка или <code>_blank</code>, <code>_self</code> и т.д.).</li>
<li><code>features</code>: Строка со списком параметров окна (размеры, полосы прокрутки и т.д.).</li>
</ul>
</li>
<li><code>window.close()</code>: Закрывает текущее окно, или окно, на которое указывает ссылка.</li>
<li><code>window.document</code>: Свойство <code>window</code> для доступа к объекту <code>document</code> текущего окна.</li>
</ul>
<hr>
<p><strong>Примеры из пособия (стр. 33-35) и их выполнение:</strong></p>
<p><strong>Пример 1 (стр. 34) - Открытие и закрытие нового окна</strong></p>
<p>Демонстрирует, как открыть новое окно с указанным HTML-файлом и размерами, а затем закрыть его по нажатию другой кнопки.</p>
<p><strong>Исходные материалы:</strong> Вам понадобится файл <code>11.html</code> (или любой другой простой HTML-файл), который будет открываться в новом окне. Создадим его для примера.</p>
<p><strong>Файл: <code>11.html</code></strong><br>
(Это будет файл, который ОТКРЫВАЕТСЯ в новом окне)</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Содержимое нового окна<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token style-attr language-css"><span class="token attr-name"> <span class="token attr-name">style</span></span><span class="token punctuation">="</span><span class="token attr-value"><span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f0f0</span><span class="token punctuation">;</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">padding-top</span><span class="token punctuation">:</span> <span class="token number">50</span>px<span class="token punctuation">;</span></span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h2</span><span class="token punctuation">&gt;</span></span>Это содержимое нового окна!<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h2</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>flower.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Цветок<span class="token punctuation">"</span></span><span class="token style-attr language-css"><span class="token attr-name"> <span class="token attr-name">style</span></span><span class="token punctuation">="</span><span class="token attr-value"><span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">80%</span><span class="token punctuation">;</span> <span class="token property">height</span><span class="token punctuation">:</span> auto<span class="token punctuation">;</span></span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Можете его закрыть, нажав кнопку в исходном окне.<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><em>Примечание: для отображения картинки <code>flower.jpg</code> вам нужен будет этот файл в той же директории, где и <code>11.html</code>. Но даже без картинки, пример будет работать.</em></p>
<p><strong>Код для Примера 1:</strong></p>
<p><strong>Файл: <code>lab4_open_close_window.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Открытие и закрытие окна<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span><span class="token property">background-color</span><span class="token punctuation">:</span>PaleGreen<span class="token punctuation">;</span><span class="token punctuation">}</span>
        <span class="token selector">input </span><span class="token punctuation">{</span><span class="token property">font-weight</span><span class="token punctuation">:</span>bold<span class="token punctuation">;</span><span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> newWin<span class="token punctuation">;</span> <span class="token comment">// Переменная для хранения ссылки на новое окно</span>

        <span class="token keyword">function</span> <span class="token function">op</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Открывается файл 11.html в новом окне размером 300x300 пикселей.</span>
            <span class="token comment">// Имя окна "www" позволит ссылаться на него позже, но в этом примере</span>
            <span class="token comment">// мы используем переменную newWin.</span>
            newWin <span class="token operator">=</span> window<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">"11.html"</span><span class="token punctuation">,</span> <span class="token string">"www"</span><span class="token punctuation">,</span> <span class="token string">"width=300,height=300"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
             <span class="token comment">// Проверяем, удалось ли открыть окно, и если нет, то выводим сообщение</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>newWin<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Не удалось открыть новое окно. Возможно, оно было заблокировано."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>

        <span class="token keyword">function</span> <span class="token function">closeNewWin</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Проверяем, существует ли ссылка на открытое окно и не закрыто ли оно уже</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>newWin <span class="token operator">&amp;&amp;</span> <span class="token operator">!</span>newWin<span class="token punctuation">.</span>closed<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                newWin<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Закрываем ранее открытое окно</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Окно для закрытия не существует или уже закрыто."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Управление окнами<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Открыть окно<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>op()<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Закрыть окно<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>closeNewWin()<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Создайте новую папку, например, <code>lab4_window</code>.</li>
<li>Внутри этой папки создайте файл <code>11.html</code> и скопируйте в него предоставленный код для <code>11.html</code>.</li>
<li>Опционально: поместите изображение <code>flower.jpg</code> в ту же папку для полноты примера.</li>
<li>В той же папке создайте файл <code>lab4_open_close_window.html</code> и скопируйте в него предоставленный код.</li>
<li>Откройте <code>lab4_open_close_window.html</code> в браузере.</li>
<li>Нажмите кнопку “Открыть окно”. Должно появиться новое всплывающее окно. Браузер может спросить разрешение на всплывающие окна. Разрешите их.</li>
<li>Нажмите кнопку “Закрыть окно” в <em>первом</em> окне. Второе окно должно закрыться.</li>
</ol>
<hr>
<p><strong>Пример 2 (стр. 35) - Динамическое формирование содержимого нового окна</strong></p>
<p>Демонстрирует, как открыть новое пустое окно, а затем динамически записать в него HTML-содержимое с помощью <code>document.write()</code> и <code>document.close()</code>.</p>
<p><strong>Код для Примера 2:</strong></p>
<p><strong>Файл: <code>lab4_dynamic_window.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Динамическое окно<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">h1 </span><span class="token punctuation">{</span><span class="token property">color</span><span class="token punctuation">:</span>red<span class="token punctuation">;</span><span class="token property">text-align</span><span class="token punctuation">:</span>center<span class="token punctuation">;</span><span class="token punctuation">}</span>
        <span class="token selector">body </span><span class="token punctuation">{</span><span class="token property">background-color</span><span class="token punctuation">:</span>PaleGreen<span class="token punctuation">;</span> <span class="token property">font-weight</span><span class="token punctuation">:</span>bold<span class="token punctuation">;</span><span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">font-weight</span><span class="token punctuation">:</span> bold<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="button"]</span> </span><span class="token punctuation">{</span> <span class="token property">font-weight</span><span class="token punctuation">:</span> bold<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> win<span class="token punctuation">;</span> <span class="token comment">// Переменная для хранения ссылки на новое окно</span>

        <span class="token keyword">function</span> <span class="token function">hello</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Получаем ссылку на текстовое поле с id 't'</span>
            <span class="token keyword">var</span> p <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'t'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token comment">// Получаем значение из текстового поля (имя человека)</span>
            <span class="token keyword">var</span> personName <span class="token operator">=</span> p<span class="token punctuation">.</span>value<span class="token punctuation">;</span>

            <span class="token comment">// Открываем новое пустое окно размерами 400x500 пикселей</span>
            win <span class="token operator">=</span> window<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"width=400,height=500"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
             <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>win<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Не удалось открыть новое окно."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Открываем документ нового окна для записи</span>
            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Формируем HTML-строку для содержимого нового окна</span>
            <span class="token keyword">var</span> htmlContent <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
                &lt;!DOCTYPE html&gt;
                &lt;html&gt;
                &lt;head&gt;
                    &lt;title&gt;Приветствие&lt;/title&gt;
                    &lt;style&gt;
                        body { background-color: lightgoldenrodyellow; font-family: Arial, sans-serif; text-align: center; }
                        h1 { color: #8B4513; margin-top: 50px; }
                        img { max-width: 150px; height: auto; margin-top: 20px; }
                        button { margin-top: 30px; padding: 10px 20px; background-color: #dc3545; color: white; border: none; cursor: pointer; border-radius: 5px; }
                        button:hover { background-color: #c82333; }
                    &lt;/style&gt;
                &lt;/head&gt;
                &lt;body&gt;
                    &lt;h1&gt;Привет, </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>personName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">!!!&lt;/h1&gt;
                    &lt;hr&gt;
                    &lt;img src="flower.jpg" alt="Цветок"&gt;
                    &lt;p&gt;Примите в подарок этот букет!&lt;/p&gt;
                    &lt;button onClick="window.close();"&gt;Закрыть окно&lt;/button&gt;
                    &lt;!-- В старых браузерах может понадобиться win.close() на кнопке, но обычно window.close() достаточно --&gt;
                &lt;/body&gt;
                &lt;/html&gt;
            `</span></span><span class="token punctuation">;</span>

            <span class="token comment">// Записываем сформированное HTML-содержимое в новое окно</span>
            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>htmlContent<span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Закрываем документ нового окна, завершая запись</span>
            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Приветствие<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>hr</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>personNameInput<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Введите ваше имя:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Горбунков Семен Семенович<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>t<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>t<span class="token punctuation">"</span></span> <span class="token attr-name">size</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>30<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Приветствие<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>hello()<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>hr</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Создайте новую папку, например, <code>lab4_dynamic_window</code>.</li>
<li>Опционально: поместите изображение <code>flower.jpg</code> (из предыдущего примера или любое другое) в эту папку для отображения в новом окне.</li>
<li>В этой папке создайте файл <code>lab4_dynamic_window.html</code> и скопируйте в него предоставленный код.</li>
<li>Откройте <code>lab4_dynamic_window.html</code> в браузере.</li>
<li>Введите имя в текстовое поле (или оставьте предложенное) и нажмите кнопку “Приветствие”. Должно появиться новое окно с динамически сгенерированным приветствием и кнопкой “Закрыть окно”.</li>
</ol>
<hr>
<p><strong>Задание 1 (стр. 36) - Вариант 1 (Формирование биографии)</strong></p>
<p><strong>Задача:</strong> Ввести данные в анкету, состоящую из текстовых полей формы, и сформировать биографию по этим данным на отдельной странице (в новом окне).</p>
<p><strong>Решено:</strong> Использование множества <code>getElementById().value</code> для сбора данных, затем формирование сложной HTML-строки и вывод её в новое окно <code>window.open().document.write()</code>.</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab4_task1_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура с формой анкеты:</strong><br>
Особое внимание уделите <code>id</code> для каждого <code>&lt;input&gt;</code> элемента, так как по ним мы будем получать значения.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Анкета для биографии<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f7f7f7</span><span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">justify-content</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">min-height</span><span class="token punctuation">:</span> <span class="token number">100</span>vh<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.container</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#e0ffe0</span><span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#c0e0c0</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">25</span>px<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">box-shadow</span><span class="token punctuation">:</span> <span class="token number">0</span> <span class="token number">4</span>px <span class="token number">8</span>px <span class="token function">rgba</span><span class="token punctuation">(</span><span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">500</span>px<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#33a033</span><span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form div </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form label </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">150</span>px<span class="token punctuation">;</span> <span class="token property">flex-shrink</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token property">font-weight</span><span class="token punctuation">:</span> bold<span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#555</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">flex-grow</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form button </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">12</span>px<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#33a033</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form button<span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#288428</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">generateBiography</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Логика будет здесь</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Анкета<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>lastName<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Фамилия:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>lastName<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Горбунков<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>firstName<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Имя:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>firstName<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Семен<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>middleName<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Отчество:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>middleName<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Семенович<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>birthYear<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Год рождения:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>birthYear<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>1990<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>birthPlace<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Место рождения:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>birthPlace<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Одесса<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>hobby<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Любимое занятие:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>hobby<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>читать<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>dislike<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Не любимое занятие:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>dislike<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>мыть посуду<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>generateBiography();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Сформировать биографию<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Сбор данных из полей формы:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Внутри generateBiography() function</span>
<span class="token keyword">var</span> lastName <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'lastName'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
<span class="token keyword">var</span> firstName <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'firstName'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
<span class="token keyword">var</span> middleName <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'middleName'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
<span class="token keyword">var</span> birthYear <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'birthYear'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
<span class="token keyword">var</span> birthPlace <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'birthPlace'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
<span class="token keyword">var</span> hobby <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'hobby'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
<span class="token keyword">var</span> dislike <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'dislike'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Валидация (опционально, но рекомендуется):</strong> Убедитесь, что все поля заполнены.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>lastName <span class="token operator">||</span> <span class="token operator">!</span>firstName <span class="token operator">||</span> <span class="token operator">!</span>middleName <span class="token operator">||</span> <span class="token operator">!</span>birthYear <span class="token operator">||</span> <span class="token operator">!</span>birthPlace <span class="token operator">||</span> <span class="token operator">!</span>hobby <span class="token operator">||</span> <span class="token operator">!</span>dislike<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Пожалуйста, заполните все поля анкеты."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">return</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Формирование HTML-содержимого биографии:</strong> Создайте шаблон HTML для нового окна, используя собранные данные.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> bioContent <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
    &lt;!DOCTYPE html&gt;
    &lt;html&gt;
    &lt;head&gt;
        &lt;title&gt;О себе - Биография&lt;/title&gt;
        &lt;style&gt;
            body { font-family: Arial, sans-serif; background-color: #f0f8ff; margin: 20px; }
            .bio-container { background-color: #ffffff; border: 1px solid #ddd; padding: 20px; border-radius: 8px; max-width: 600px; margin: 20px auto; box-shadow: 0 2px 4px rgba(0,0,0,0.1); }
            h1 { text-align: center; color: #333; }
            p { font-size: 1.1em; line-height: 1.6; color: #555; }
            button { display: block; margin: 20px auto; padding: 10px 20px; background-color: #6c757d; color: white; border: none; border-radius: 5px; cursor: pointer; }
            button:hover { background-color: #5a6268; }
        &lt;/style&gt;
    &lt;/head&gt;
    &lt;body&gt;
        &lt;div class="bio-container"&gt;
            &lt;h1&gt;О себе&lt;/h1&gt;
            &lt;p&gt;Я, </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>lastName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>firstName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>middleName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> родился в </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>birthYear<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> году в городе </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>birthPlace<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">.&lt;/p&gt;
            &lt;p&gt;Больше всего я люблю </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>hobby<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> и очень не люблю </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>dislike<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">. Было бы замечательно, всю жизнь только </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>hobby<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">, но к сожалению приходится иногда и </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>dislike<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">.&lt;/p&gt;
            &lt;button onClick="window.close();"&gt;закрыть&lt;/button&gt;
        &lt;/div&gt;
    &lt;/body&gt;
    &lt;/html&gt;
`</span></span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Открытие нового окна и запись биографии:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> biographyWindow <span class="token operator">=</span> window<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"_blank"</span><span class="token punctuation">,</span> <span class="token string">"width=700,height=500,scrollbars=yes,resizable=yes"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>biographyWindow<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Не удалось открыть новое окно."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">return</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
biographyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
biographyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>bioContent<span class="token punctuation">)</span><span class="token punctuation">;</span>
biographyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab4_task1_var1.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Анкета для биографии<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f7f7f7</span><span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">justify-content</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">min-height</span><span class="token punctuation">:</span> <span class="token number">100</span>vh<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.container</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#e0ffe0</span><span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#c0e0c0</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">25</span>px<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">box-shadow</span><span class="token punctuation">:</span> <span class="token number">0</span> <span class="token number">4</span>px <span class="token number">8</span>px <span class="token function">rgba</span><span class="token punctuation">(</span><span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">500</span>px<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#33a033</span><span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form div </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form label </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">150</span>px<span class="token punctuation">;</span> <span class="token property">flex-shrink</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token property">font-weight</span><span class="token punctuation">:</span> bold<span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#555</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">flex-grow</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form button </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">12</span>px<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#33a033</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form button<span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#288428</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">generateBiography</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> lastName <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'lastName'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> firstName <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'firstName'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> middleName <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'middleName'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> birthYear <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'birthYear'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> birthPlace <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'birthPlace'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> hobby <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'hobby'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> dislike <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'dislike'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>lastName <span class="token operator">||</span> <span class="token operator">!</span>firstName <span class="token operator">||</span> <span class="token operator">!</span>middleName <span class="token operator">||</span> <span class="token operator">!</span>birthYear <span class="token operator">||</span> <span class="token operator">!</span>birthPlace <span class="token operator">||</span> <span class="token operator">!</span>hobby <span class="token operator">||</span> <span class="token operator">!</span>dislike<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Пожалуйста, заполните все поля анкеты."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token keyword">var</span> bioContent <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
                &lt;!DOCTYPE html&gt;
                &lt;html&gt;
                &lt;head&gt;
                    &lt;title&gt;О себе - Биография&lt;/title&gt;
                    &lt;style&gt;
                        body { font-family: Arial, sans-serif; background-color: #f0f8ff; margin: 20px; }
                        .bio-container { background-color: #ffffff; border: 1px solid #ddd; padding: 20px; border-radius: 8px; max-width: 600px; margin: 20px auto; box-shadow: 0 2px 4px rgba(0,0,0,0.1); }
                        h1 { text-align: center; color: #333; }
                        p { font-size: 1.1em; line-height: 1.6; color: #555; }
                        button { display: block; margin: 20px auto; padding: 10px 20px; background-color: #6c757d; color: white; border: none; border-radius: 5px; cursor: pointer; }
                        button:hover { background-color: #5a6268; }
                    &lt;/style&gt;
                &lt;/head&gt;
                &lt;body&gt;
                    &lt;div class="bio-container"&gt;
                        &lt;h1&gt;О себе&lt;/h1&gt;
                        &lt;p&gt;Я, </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>lastName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>firstName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>middleName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> родился в </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>birthYear<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> году в городе </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>birthPlace<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">.&lt;/p&gt;
                        &lt;p&gt;Больше всего я люблю </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>hobby<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> и очень не люблю </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>dislike<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">. Было бы замечательно, всю жизнь только </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>hobby<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">, но к сожалению приходится иногда и </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>dislike<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">.&lt;/p&gt;
                        &lt;button onClick="window.close();"&gt;закрыть&lt;/button&gt;
                    &lt;/div&gt;
                &lt;/body&gt;
                &lt;/html&gt;
            `</span></span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> biographyWindow <span class="token operator">=</span> window<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"_blank"</span><span class="token punctuation">,</span> <span class="token string">"width=700,height=500,scrollbars=yes,resizable=yes"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>biographyWindow<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Не удалось открыть новое окно. Проверьте, не блокирует ли браузер всплывающие окна."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            biographyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            biographyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>bioContent<span class="token punctuation">)</span><span class="token punctuation">;</span>
            biographyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Анкета<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>lastName<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Фамилия:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>lastName<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Горбунков<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>firstName<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Имя:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>firstName<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Семен<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>middleName<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Отчество:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>middleName<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Семенович<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>birthYear<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Год рождения:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>birthYear<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>1990<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>birthPlace<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Место рождения:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>birthPlace<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Одесса<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>hobby<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Любимое занятие:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>hobby<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>читать<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>dislike<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Не любимое занятие:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>dislike<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>мыть посуду<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>generateBiography();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Сформировать биографию<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab4_task1_var1.html</code> в браузере. Заполните анкету и нажмите кнопку.</p>
</li>
</ol>
<hr>
<p><strong>Задание 2 (стр. 37) - Вариант 2 (Генератор сказок)</strong></p>
<p><strong>Задача:</strong> Создать генератор сказок. Ввод данных (имя героя, любимое занятие, друг героя, любимый подарок) в текстовые поля формы. Сгенерированную сказку вывести в другое окно.</p>
<p><strong>Решено:</strong> Аналогично Заданию 1, но с другим набором данных и текстом сказки.</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab4_task2_var2.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура с формой для генератора сказок:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Генератор сказок<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f7f0</span><span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">justify-content</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">min-height</span><span class="token punctuation">:</span> <span class="token number">100</span>vh<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.container</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#dff0d8</span><span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#c8e5bc</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">25</span>px<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">box-shadow</span><span class="token punctuation">:</span> <span class="token number">0</span> <span class="token number">4</span>px <span class="token number">8</span>px <span class="token function">rgba</span><span class="token punctuation">(</span><span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">500</span>px<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#3c763d</span><span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form div </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form label </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">150</span>px<span class="token punctuation">;</span> <span class="token property">flex-shrink</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token property">font-weight</span><span class="token punctuation">:</span> bold<span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#5cb85c</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">flex-grow</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form button </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">12</span>px<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#5cb85c</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form button<span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#4cae4c</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">generateStory</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Логика будет здесь</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Генератор сказок<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>heroName<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Имя героя:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>heroName<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>пташка<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>favoriteActivity<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Любимое занятие:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>favoriteActivity<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>петь<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>friendName<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Друг героя:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>friendName<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>дятел<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>favoriteGift<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Любимый подарок:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>favoriteGift<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>цветы<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>generateStory();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Сгенерировать сказку<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Сбор данных и валидация:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// Внутри generateStory() function</span>
<span class="token keyword">var</span> heroName <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'heroName'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> favoriteActivity <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'favoriteActivity'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> friendName <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'friendName'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> favoriteGift <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'favoriteGift'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>heroName <span class="token operator">||</span> <span class="token operator">!</span>favoriteActivity <span class="token operator">||</span> <span class="token operator">!</span>friendName <span class="token operator">||</span> <span class="token operator">!</span>favoriteGift<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Пожалуйста, заполните все поля для генерации сказки."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">return</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
</li>
<li>
<p><strong>Формирование текста сказки:</strong> Используйте собранные переменные для построения сюжета.</p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> story <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
    В одном лесу жила маленькая </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">, которая очень любила </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteActivity<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> чудесные песни.
    У нее так хорошо получалось, что весь лес собирался послушать ее! От сороки она узнала,
    что у людей принято дарить </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteGift<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> любимым исполнителям. А </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteGift<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> она любила также сильно, как и </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteActivity<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">.
    Долго грустила </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">. Но однажды, после очередного импровизированного концерта,
    </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>friendName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> подлетел к </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> и подарил ей... </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteGift<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">! Уж он то был истинным джентльменом!
    </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> была невероятно счастлива!!!
`</span></span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Формирование HTML-содержимого нового окна и его открытие:</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token keyword">var</span> storyContent <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
    &lt;!DOCTYPE html&gt;
    &lt;html&gt;
    &lt;head&gt;
        &lt;title&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> и </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteGift<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/title&gt;
        &lt;style&gt;
            body { font-family: Arial, sans-serif; background-color: #fffacd; margin: 20px; }
            .story-container { background-color: #ffffff; border: 1px solid #e0c98f; padding: 20px; border-radius: 8px; max-width: 600px; margin: 20px auto; box-shadow: 0 2px 4px rgba(0,0,0,0.1); }
            h1 { text-align: center; color: #8b4513; }
            p { font-size: 1.1em; line-height: 1.6; color: #555; text-indent: 1.5em; text-align: justify; }
            button { display: block; margin: 20px auto; padding: 10px 20px; background-color: #6c757d; color: white; border: none; border-radius: 5px; cursor: pointer; }
            button:hover { background-color: #5a6268; }
        &lt;/style&gt;
    &lt;/head&gt;
    &lt;body&gt;
        &lt;div class="story-container"&gt;
            &lt;h1&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> и </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteGift<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/h1&gt;
            &lt;p&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>story<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/p&gt;
            &lt;button onClick="window.close();"&gt;закрыть&lt;/button&gt;
        &lt;/div&gt;
    &lt;/body&gt;
    &lt;/html&gt;
`</span></span><span class="token punctuation">;</span>

<span class="token keyword">var</span> storyWindow <span class="token operator">=</span> window<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"_blank"</span><span class="token punctuation">,</span> <span class="token string">"width=700,height=500,scrollbars=yes,resizable=yes"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>storyWindow<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Не удалось открыть новое окно. Проверьте, не блокирует ли браузер всплывающие окна."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">return</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
storyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
storyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>storyContent<span class="token punctuation">)</span><span class="token punctuation">;</span>
storyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Полный код <code>lab4_task2_var2.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Генератор сказок<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f7f0</span><span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">justify-content</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">min-height</span><span class="token punctuation">:</span> <span class="token number">100</span>vh<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.container</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#dff0d8</span><span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#c8e5bc</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">25</span>px<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">box-shadow</span><span class="token punctuation">:</span> <span class="token number">0</span> <span class="token number">4</span>px <span class="token number">8</span>px <span class="token function">rgba</span><span class="token punctuation">(</span><span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">500</span>px<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#3c763d</span><span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form div </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form label </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">150</span>px<span class="token punctuation">;</span> <span class="token property">flex-shrink</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token property">font-weight</span><span class="token punctuation">:</span> bold<span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#5cb85c</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">flex-grow</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form button </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">12</span>px<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#5cb85c</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form button<span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#4cae4c</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">generateStory</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> heroName <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'heroName'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> favoriteActivity <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'favoriteActivity'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> friendName <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'friendName'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> favoriteGift <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'favoriteGift'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>heroName <span class="token operator">||</span> <span class="token operator">!</span>favoriteActivity <span class="token operator">||</span> <span class="token operator">!</span>friendName <span class="token operator">||</span> <span class="token operator">!</span>favoriteGift<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Пожалуйста, заполните все поля для генерации сказки."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token keyword">var</span> story <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
                В одном лесу жила маленькая </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">, которая очень любила </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteActivity<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> чудесные песни.
                У нее так хорошо получалось, что весь лес собирался послушать ее! От сороки она узнала,
                что у людей принято дарить </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteGift<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> любимым исполнителям. А </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteGift<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> она любила также сильно, как и </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteActivity<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">.
                Долго грустила </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">. Но однажды, после очередного импровизированного концерта,
                </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>friendName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> подлетел к </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> и подарил ей... </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteGift<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">! Уж он то был истинным джентльменом!
                </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> была невероятно счастлива!!!
            `</span></span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> storyContent <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
                &lt;!DOCTYPE html&gt;
                &lt;html&gt;
                &lt;head&gt;
                    &lt;title&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> и </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteGift<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/title&gt;
                    &lt;style&gt;
                        body { font-family: Arial, sans-serif; background-color: #fffacd; margin: 20px; }
                        .story-container { background-color: #ffffff; border: 1px solid #e0c98f; padding: 20px; border-radius: 8px; max-width: 600px; margin: 20px auto; box-shadow: 0 2px 4px rgba(0,0,0,0.1); }
                        h1 { text-align: center; color: #8b4513; }
                        p { font-size: 1.1em; line-height: 1.6; color: #555; text-indent: 1.5em; text-align: justify; }
                        button { display: block; margin: 20px auto; padding: 10px 20px; background-color: #6c757d; color: white; border: none; border-radius: 5px; cursor: pointer; }
                        button:hover { background-color: #5a6268; }
                    &lt;/style&gt;
                &lt;/head&gt;
                &lt;body&gt;
                    &lt;div class="story-container"&gt;
                        &lt;h1&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>heroName<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> и </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>favoriteGift<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/h1&gt;
                        &lt;p&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>story<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/p&gt;
                        &lt;button onClick="window.close();"&gt;закрыть&lt;/button&gt;
                    &lt;/div&gt;
                &lt;/body&gt;
                &lt;/html&gt;
            `</span></span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> storyWindow <span class="token operator">=</span> window<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"_blank"</span><span class="token punctuation">,</span> <span class="token string">"width=700,height=500,scrollbars=yes,resizable=yes"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>storyWindow<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Не удалось открыть новое окно. Проверьте, не блокирует ли браузер всплывающие окна."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            storyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            storyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>storyContent<span class="token punctuation">)</span><span class="token punctuation">;</span>
            storyWindow<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Генератор сказок<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>heroName<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Имя героя:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>heroName<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>пташка<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>favoriteActivity<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Любимое занятие:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>favoriteActivity<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>петь<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>friendName<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Друг героя:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>friendName<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>дятел<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>favoriteGift<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Любимый подарок:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>favoriteGift<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>цветы<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>generateStory();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Сгенерировать сказку<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab4_task2_var2.html</code> в браузере. Заполните поля и сгенерируйте сказку.</p>
</li>
</ol>
<hr>
<p><strong>Задание 3 (стр. 60) - Вариант 1 (Динамическая галерея с изменением рамки)</strong></p>
<p><strong>Задача:</strong> Создать документ, в котором рисунок <code>neznakomka3.jpg</code> заключен в рамку серого цвета типа <code>inset</code> и толщиной 50. По нажатию кнопки изменять цвет рамки на синий и надпись на кнопке. При следующем нажатии изменять цвет рамки на серый и надпись на кнопке.</p>
<p><strong>Решено:</strong> Использование <code>getElementById()</code> для доступа к изображению (<code>img</code>) и кнопке (<code>button</code>). Изменение стиля <code>border</code> изображения и <code>value</code> кнопки. Переключение состояния (цвета рамки и текста кнопки) с помощью переменной-флага.</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>neznakomka3.jpg</code> (любое изображение, можно использовать своё и переименовать).</li>
</ul>
</li>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab4_task3_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Изменение рамки изображения<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">50</span>px<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f0f0</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">img </span><span class="token punctuation">{</span>
            <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">50</span>px inset grey<span class="token punctuation">;</span> <span class="token comment">/* Исходный стиль рамки */</span>
            <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">/* Убираем отступы, если есть */</span>
        <span class="token punctuation">}</span>
        <span class="token selector">button </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> isBlue <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span> <span class="token comment">// Флаг для отслеживания текущего цвета рамки</span>

        <span class="token keyword">function</span> <span class="token function">toggleBorder</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> img <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'myImage'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> button <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'toggleButton'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>isBlue<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token comment">// Сейчас синий, меняем на серый</span>
                img<span class="token punctuation">.</span>style<span class="token punctuation">.</span>borderColor <span class="token operator">=</span> <span class="token string">'grey'</span><span class="token punctuation">;</span>
                button<span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">'Изменить рамку на синий'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token comment">// Сейчас серый, меняем на синий</span>
                img<span class="token punctuation">.</span>style<span class="token punctuation">.</span>borderColor <span class="token operator">=</span> <span class="token string">'blue'</span><span class="token punctuation">;</span>
                button<span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">'Изменить рамку на серый'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            isBlue <span class="token operator">=</span> <span class="token operator">!</span>isBlue<span class="token punctuation">;</span> <span class="token comment">// Переключаем флаг</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Изменение рамки изображения<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>myImage<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>neznakomka3.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Красивая картина<span class="token punctuation">"</span></span> <span class="token attr-name">width</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>300<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggleButton<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggleBorder();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Изменить рамку на синий<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображение <code>neznakomka3.jpg</code></strong> (или переименуйте ваше) в ту же папку, где и <code>lab4_task3_var1.html</code>.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab4_task3_var1.html</code> в браузере. Нажимайте кнопку и наблюдайте за изменением цвета рамки и текста кнопки.</p>
</li>
</ol>
<hr>
<p><strong>Задание 2 (стр. 60) - Вариант 1 (Показать/Скрыть свечу)</strong></p>
<p><strong>Задача:</strong> Сначала на странице только текст стихотворения и кнопка с надписью «показать свечу». При нажатии на кнопку текст стихотворения прячется, на его месте появляется рисунок, и надпись на кнопке меняется на «показать текст». Если еще раз нажать на кнопку, рисунок исчезает и появляется текст.</p>
<p><strong>Решено:</strong> Использование свойства CSS <code>display</code> (<code>block</code> для показа, <code>none</code> для скрытия) для переключения видимости элементов.</p>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>свеча1.gif</code> (любое изображение свечи).</li>
<li>Текст стихотворения (например, из файла <code>Анненский.doc</code>, но можно просто вставить прямо в HTML).</li>
</ul>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab4_task2_var1.html</code>.</p>
</li>
<li>
<p><strong>Задайте стили для текста и картинки:</strong></p>
<ul>
<li>Создайте <code>&lt;p&gt;</code> для текста и <code>&lt;img&gt;</code> для картинки, присвоив им <code>id</code>.</li>
<li>Изначально картинка должна быть скрыта (<code>display: none;</code>).</li>
<li>Добавьте стили для фона страницы, шрифта и рамок, как указано в задании.</li>
</ul>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Свеча и Стихотворение<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> 
            <span class="token property">background-color</span><span class="token punctuation">:</span> darkblue<span class="token punctuation">;</span> <span class="token comment">/* Темно-синий фон */</span>
            <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> 
            <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">22</span>px<span class="token punctuation">;</span> <span class="token comment">/* Размер шрифта */</span>
            <span class="token property">font-style</span><span class="token punctuation">:</span> italic<span class="token punctuation">;</span> <span class="token comment">/* Курсив */</span>
            <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token comment">/* Цвет шрифта белый */</span>
            <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span>
            <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.content-container</span> </span><span class="token punctuation">{</span>
            <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">600</span>px<span class="token punctuation">;</span>
            <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span>
            <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span>
            <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">5</span>px outset <span class="token hexcode">#ffA089</span><span class="token punctuation">;</span> <span class="token comment">/* Рамка вокруг текста/картинки */</span>
            <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#text-content</span> </span><span class="token punctuation">{</span>
            <span class="token comment">/* Стиль для текста */</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#image-content</span> </span><span class="token punctuation">{</span>
            <span class="token property">display</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span> <span class="token comment">/* Изначально скрыто */</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#image-content</span> img </span><span class="token punctuation">{</span>
            <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">200</span>px<span class="token punctuation">;</span> <span class="token comment">/* Размер картинки */</span>
            <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">200</span>px<span class="token punctuation">;</span> <span class="token comment">/* Размер картинки */</span>
            <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">50</span>px outset <span class="token hexcode">#ffA089</span><span class="token punctuation">;</span> <span class="token comment">/* Рамка вокруг картинки, толщина 50 */</span>
            <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token comment">/* Отступы по 5 */</span>
            <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector">button </span><span class="token punctuation">{</span>
            <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">20</span>px<span class="token punctuation">;</span>
            <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">18</span>px<span class="token punctuation">;</span>
            <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span>
            <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> showingText <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span> <span class="token comment">// Флаг: true - показывается текст, false - показывается картинка</span>

        <span class="token keyword">function</span> <span class="token function">toggleContent</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> textDiv <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'text-content'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> imageDiv <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'image-content'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> toggleButton <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'toggle-button'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>showingText<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token comment">// Скрываем текст, показываем картинку</span>
                textDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'none'</span><span class="token punctuation">;</span>
                imageDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'block'</span><span class="token punctuation">;</span>
                toggleButton<span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">'Показать текст'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token comment">// Скрываем картинку, показываем текст</span>
                imageDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'block'</span><span class="token punctuation">;</span> <span class="token comment">// Make sure container is block before setting its children</span>
                imageDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'none'</span><span class="token punctuation">;</span> <span class="token comment">// Temporarily hide image, so text takes up space.</span>
                textDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'block'</span><span class="token punctuation">;</span> <span class="token comment">// Show text again.</span>
                toggleButton<span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">'Показать свечу'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            showingText <span class="token operator">=</span> <span class="token operator">!</span>showingText<span class="token punctuation">;</span> <span class="token comment">// Переключаем флаг</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>content-container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text-content<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h3</span><span class="token punctuation">&gt;</span></span>Иннокентий Анненский<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h3</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h2</span><span class="token punctuation">&gt;</span></span>Свечку внесли<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h2</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Не мерещится ль вам иногда,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Когда сумерки ходят по дому,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Тут же возле иная среда,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Где живем мы совсем по-другому?<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>С тенью тень там так мягко слилась,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Там бывает такая минута,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Что лучами незримыми глаз<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Мы уходим друг в друга как будто.<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>И движеньем спугнуть этот миг<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Мы боимся, иль словом нарушить,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Точно ухом кто возле приник,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Заставляя далекое слушать.<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Но едва запылает свеча,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Чуткий мир уступает без боя,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Лишь из глаз по наклонам луча<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Тени в пламя сбегут голубое.<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>image-content<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>свеча1.gif<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Свеча<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggle-button<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggleContent();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Показать свечу<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображение <code>свеча1.gif</code></strong> в ту же папку, где и <code>lab4_task2_var1.html</code>.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab4_task2_var1.html</code> в браузере. Нажимайте кнопку для переключения между текстом и изображением.</p>
</li>
</ol>
<hr>
<p><strong>Задание 3 (стр. 60) - Вариант 1 (Движение картинки)</strong></p>
<p><strong>Задача:</strong> Создать документ, в котором рисунок <code>p5_0.jpg</code> занимает 50% окна и является нижним слоем. На верхнем слое второй рисунок <code>4.gif</code>, который двигается по горизонтали к правой границе первого рисунка, затем на строку (высоту рисунка) вниз и назад, к левой границе, на строку вниз и к правой границе, и т.д. до нижней границы первого рисунка.</p>
<p><strong>Решено:</strong> Использование JavaScript-функции, вызываемой по <code>setTimeout()</code>, для изменения свойств <code>top</code> и <code>left</code> второго изображения (<code>position: absolute;</code>). Будет использоваться переменная <code>s</code> для шага и <code>direction</code> для изменения направления движения.</p>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>p5_0.jpg</code> (фоновое изображение)</li>
<li><code>4.gif</code> (движущееся изображение)</li>
</ul>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab4_task3_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура и CSS-позиционирование:</strong><br>
<code>p5_0.jpg</code> будет фоном, <code>4.gif</code> будет абсолютно позиционирован для движения.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Движение картинки<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token property">overflow</span><span class="token punctuation">:</span> hidden<span class="token punctuation">;</span> <span class="token comment">/* Убираем прокрутку, если картинки выходят за край */</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#background-image</span> </span><span class="token punctuation">{</span>
            <span class="token property">position</span><span class="token punctuation">:</span> absolute<span class="token punctuation">;</span>
            <span class="token property">top</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
            <span class="token property">left</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
            <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token comment">/* Ширина на весь экран */</span>
            <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token comment">/* Высота на весь экран */</span>
            <span class="token property">object-fit</span><span class="token punctuation">:</span> cover<span class="token punctuation">;</span> <span class="token comment">/* Чтобы фон заполнял, но не искажался */</span>
            <span class="token property">z-index</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">/* Нижний слой */</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#moving-image</span> </span><span class="token punctuation">{</span>
            <span class="token property">position</span><span class="token punctuation">:</span> absolute<span class="token punctuation">;</span>
            <span class="token property">top</span><span class="token punctuation">:</span> <span class="token number">0</span>px<span class="token punctuation">;</span> <span class="token comment">/* Начальная позиция */</span>
            <span class="token property">left</span><span class="token punctuation">:</span> <span class="token number">0</span>px<span class="token punctuation">;</span> <span class="token comment">/* Начальная позиция */</span>
            <span class="token property">z-index</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">;</span> <span class="token comment">/* Верхний слой */</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> movingImage<span class="token punctuation">;</span> <span class="token comment">// Ссылка на двигающееся изображение</span>
        <span class="token keyword">var</span> backgroundImage<span class="token punctuation">;</span> <span class="token comment">// Ссылка на фоновое изображение</span>
        <span class="token keyword">var</span> step <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">;</span> <span class="token comment">// Шаг движения в пикселях</span>
        <span class="token keyword">var</span> currentX <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> currentY <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> directionX <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// 1 для движения вправо, -1 для движения влево</span>
        <span class="token keyword">var</span> directionY <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// 1 для движения вниз, -1 для движения вверх</span>
        <span class="token keyword">var</span> state <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// 0: вправо, 1: вниз+влево, 2: вниз+вправо (упрощение логики)</span>
        
        <span class="token comment">// Получаем ссылки на элементы после загрузки DOM</span>
        window<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            movingImage <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'moving-image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            backgroundImage <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'background-image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token function">moveImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Запускаем движение</span>
        <span class="token punctuation">}</span><span class="token punctuation">;</span>

        <span class="token keyword">function</span> <span class="token function">moveImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> bgWidth <span class="token operator">=</span> backgroundImage<span class="token punctuation">.</span>offsetWidth<span class="token punctuation">;</span>
            <span class="token keyword">var</span> bgHeight <span class="token operator">=</span> backgroundImage<span class="token punctuation">.</span>offsetHeight<span class="token punctuation">;</span>
            <span class="token keyword">var</span> imgWidth <span class="token operator">=</span> movingImage<span class="token punctuation">.</span>offsetWidth<span class="token punctuation">;</span>
            <span class="token keyword">var</span> imgHeight <span class="token operator">=</span> movingImage<span class="token punctuation">.</span>offsetHeight<span class="token punctuation">;</span>

            <span class="token comment">// Логика движения по траектории из задания:</span>
            <span class="token comment">// 1. По горизонтали вправо до правой границы</span>
            <span class="token comment">// 2. Вниз на высоту рисунка, затем назад к левой границе</span>
            <span class="token comment">// 3. Вниз на высоту рисунка, затем к правой границе</span>
            <span class="token comment">// ... до нижней границы</span>
            
            <span class="token comment">// Это сложная траектория. Для простоты и соответствия примеру:</span>
            <span class="token comment">// Двигается по горизонтали до правого края, затем меняет направление и продолжает вниз.</span>
            <span class="token comment">// В оригинальном задании (стр. 59) "движется по главной диагонали ... затем вверх ... снова вниз" - это другое.</span>
            <span class="token comment">// Мы будем реализовывать движение по горизонтали + смещение вниз, основываясь на описании Задания 3</span>
            <span class="token comment">// из Лабораторной 4, Вариант 1 (стр. 60).</span>

            <span class="token comment">// Предполагаем, что движение идет последовательными "отрезками":</span>
            <span class="token comment">// 1. Вправо</span>
            <span class="token comment">// 2. Вниз</span>
            <span class="token comment">// 3. Влево</span>
            <span class="token comment">// 4. Вниз</span>
            <span class="token comment">// 5. Вправо</span>
            <span class="token comment">// ... и так чередуются горизонтальные движения и вертикальные смещения.</span>

            currentX <span class="token operator">+=</span> step <span class="token operator">*</span> directionX<span class="token punctuation">;</span>
            
            <span class="token comment">// Проверяем, достигли ли границы по X</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>directionX <span class="token operator">===</span> <span class="token number">1</span> <span class="token operator">&amp;&amp;</span> currentX <span class="token operator">+</span> imgWidth <span class="token operator">&gt;=</span> bgWidth<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Движение вправо, достигли правого края</span>
                currentX <span class="token operator">=</span> bgWidth <span class="token operator">-</span> imgWidth<span class="token punctuation">;</span> <span class="token comment">// Устанавливаем точно у края</span>
                directionX <span class="token operator">=</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Меняем направление на влево</span>
                currentY <span class="token operator">+=</span> imgHeight<span class="token punctuation">;</span> <span class="token comment">// Сдвиг вниз на высоту рисунка</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>directionX <span class="token operator">===</span> <span class="token operator">-</span><span class="token number">1</span> <span class="token operator">&amp;&amp;</span> currentX <span class="token operator">&lt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Движение влево, достигли левого края</span>
                currentX <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Устанавливаем точно у края</span>
                directionX <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Меняем направление на вправо</span>
                currentY <span class="token operator">+=</span> imgHeight<span class="token punctuation">;</span> <span class="token comment">// Сдвиг вниз на высоту рисунка</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Проверяем, достигли ли нижней границы общего рисунка</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>currentY <span class="token operator">+</span> imgHeight <span class="token operator">&gt;=</span> bgHeight<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                currentY <span class="token operator">=</span> bgHeight <span class="token operator">-</span> imgHeight<span class="token punctuation">;</span> <span class="token comment">// Устанавливаем точно у нижнего края</span>
                <span class="token comment">// Здесь можно остановить движение, или начать заново сверху</span>
                console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Достигнута нижняя граница. Остановка."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span> <span class="token comment">// Останавливаем движение</span>
            <span class="token punctuation">}</span>

            movingImage<span class="token punctuation">.</span>style<span class="token punctuation">.</span>left <span class="token operator">=</span> currentX <span class="token operator">+</span> <span class="token string">'px'</span><span class="token punctuation">;</span>
            movingImage<span class="token punctuation">.</span>style<span class="token punctuation">.</span>top <span class="token operator">=</span> currentY <span class="token operator">+</span> <span class="token string">'px'</span><span class="token punctuation">;</span>

            <span class="token comment">// Вызываем эту же функцию через небольшой интервал</span>
            <span class="token function">setTimeout</span><span class="token punctuation">(</span>moveImage<span class="token punctuation">,</span> <span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Интервал в мс для плавности</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>background-image<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>p5_0.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Фон<span class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>moving-image<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>4.gif<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Движущаяся картинка<span class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображения <code>p5_0.jpg</code> и <code>4.gif</code></strong> в ту же папку, где и <code>lab4_task3_var1.html</code>.<br>
<em>Примечание</em>: Вы можете настроить размеры изображений в CSS или сами файлы, чтобы они выглядели хорошо на вашей странице.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab4_task3_var1.html</code> в браузере. Вы должны увидеть, как <code>4.gif</code> движется по заданной траектории.</p>
</li>
</ol>
<hr>
<p>Это завершает <strong>ЛАБОРАТОРНУЮ РАБОТУ № 4</strong>.</p>
<p>Отлично! Переходим к <strong>ЛАБОРАТОРНОЙ РАБОТЕ № 5: Обращение к элементам формы – флажки, радиокнопки, списки</strong>.</p>
<hr>
<h3 id="лабораторная-работа-№-5-обращение-к-элементам-формы-–-флажки-радиокнопки-списки"><strong>ЛАБОРАТОРНАЯ РАБОТА № 5: Обращение к элементам формы – флажки, радиокнопки, списки</strong></h3>
<p><strong>Цель:</strong> Изучить, как взаимодействовать с различными элементами HTML-форм, такими как флажки (<code>checkbox</code>), радиокнопки (<code>radio button</code>) и выпадающие списки (<code>select</code>/<code>option</code>) с помощью JavaScript. Основное внимание будет уделено свойству <code>checked</code> для флажков и радиокнопок, а также свойству <code>selected</code> и <code>text</code> для элементов списка.</p>
<p><strong>Общее описание:</strong></p>
<ul>
<li><strong>Флажки (<code>&lt;input type="checkbox"&gt;</code>):</strong> Позволяют выбрать несколько опций. Состояние хранится в свойстве <code>checked</code> (<code>true</code>/<code>false</code>).</li>
<li><strong>Радиокнопки (<code>&lt;input type="radio"&gt;</code>):</strong> Позволяют выбрать только одну опцию из группы (с одинаковым <code>name</code>). Состояние также в <code>checked</code>.</li>
<li><strong>Выпадающие списки (<code>&lt;select&gt;</code> и <code>&lt;option&gt;</code>):</strong> Позволяют выбрать одну или несколько опций из списка. Для <code>&lt;option&gt;</code> важны свойства <code>selected</code> (<code>true</code>/<code>false</code>) и <code>text</code> (видимый текст опции).</li>
<li><strong><code>document.getElementById()</code>:</strong> Используется для получения элементов формы по их <code>id</code>.</li>
<li><strong>Динамический вывод:</strong> Результаты будут выводиться в <code>alert()</code> или в новые окна (<code>window.open()</code>).</li>
</ul>
<hr>
<p><strong>Примеры из пособия (стр. 39-44) и их выполнение:</strong></p>
<p><strong>Пример 1 (стр. 39) - Проверка таблицы умножения (Checkbox)</strong></p>
<p>Демонстрирует, как проверить состояние флажков (<code>checked</code>) и вывести результат в текстовое поле.</p>
<p><strong>Код для Примера 1:</strong></p>
<p><strong>Файл: <code>lab5_checkbox_check.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Проверка таблицы умножения<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">checkAll</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> ans <span class="token operator">=</span> <span class="token string">'не верно'</span><span class="token punctuation">;</span> <span class="token comment">// Изначально предполагаем ошибку</span>

            <span class="token comment">// Получаем ссылки на флажки по их id</span>
            <span class="token keyword">var</span> p1 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'c1'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 2*2=4</span>
            <span class="token keyword">var</span> p2 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'c2'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 2*5=30 (неверно)</span>
            <span class="token keyword">var</span> p3 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'c3'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 6*8=48</span>

            <span class="token comment">// Условие правильности:</span>
            <span class="token comment">// 2*2=4 (c1) = true</span>
            <span class="token comment">// 2*5=30 (c2) = false (должен быть не отмечен)</span>
            <span class="token comment">// 6*8=48 (c3) = true</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>p1<span class="token punctuation">.</span>checked <span class="token operator">&amp;&amp;</span> <span class="token operator">!</span>p2<span class="token punctuation">.</span>checked <span class="token operator">&amp;&amp;</span> p3<span class="token punctuation">.</span>checked<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                ans <span class="token operator">=</span> <span class="token string">'верно'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Вывод результата в текстовое поле с id 'result'</span>
            <span class="token keyword">var</span> p4 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'result'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            p4<span class="token punctuation">.</span>value <span class="token operator">=</span> ans<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Проверка таблицы умножения<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Отметьте правильные утверждения:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>checkbox<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c1<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c1<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>2*2=4<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c1<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>2*2=4<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>checkbox<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c2<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c2<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>2*5=30<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c2<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>2*5=30<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>checkbox<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c3<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c3<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>6*8=48<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c3<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>6*8=48<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Проверить<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>checkAll();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>result<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>result<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab5_checkbox_check.html</code>.</li>
<li>Откройте файл в браузере.</li>
<li>Попробуйте разные комбинации отметок и нажмите “Проверить”. Убедитесь, что “верно” появится только при отмеченных <code>2*2=4</code> и <code>6*8=48</code> и не отмеченном <code>2*5=30</code>.</li>
</ol>
<hr>
<p><strong>Пример 2 (стр. 40) - Проверка таблицы умножения в новом окне (Checkbox)</strong></p>
<p>Модификация Примера 1, где результат выводится в новое окно.</p>
<p><strong>Код для Примера 2:</strong></p>
<p><strong>Файл: <code>lab5_checkbox_new_window.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Проверка таблицы умножения (новое окно)<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">checkAll</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> ans <span class="token operator">=</span> <span class="token string">'не верно'</span><span class="token punctuation">;</span> <span class="token comment">// Изначально предполагаем ошибку</span>

            <span class="token keyword">var</span> p1 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'c1'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 2*2=4</span>
            <span class="token keyword">var</span> p2 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'c2'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 2*5=30 (неверно)</span>
            <span class="token keyword">var</span> p3 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'c3'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 6*8=48</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>p1<span class="token punctuation">.</span>checked <span class="token operator">&amp;&amp;</span> <span class="token operator">!</span>p2<span class="token punctuation">.</span>checked <span class="token operator">&amp;&amp;</span> p3<span class="token punctuation">.</span>checked<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                ans <span class="token operator">=</span> <span class="token string">'верно'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Открываем новое окно</span>
            <span class="token keyword">var</span> win <span class="token operator">=</span> window<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"width=300,height=150"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>win<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Не удалось открыть новое окно."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Открываем документ для записи</span>
            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Формируем HTML-строку для нового окна</span>
            <span class="token keyword">var</span> htmlContent <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
                &lt;!DOCTYPE html&gt;
                &lt;html&gt;
                &lt;head&gt;
                    &lt;title&gt;Результат проверки&lt;/title&gt;
                    &lt;style&gt;
                        body { font-family: Arial, sans-serif; text-align: center; margin-top: 30px; }
                        h1 { color: </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>ans <span class="token operator">===</span> <span class="token string">'верно'</span> <span class="token operator">?</span> <span class="token string">'green'</span> <span class="token punctuation">:</span> <span class="token string">'red'</span><span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">; }
                        button { margin-top: 20px; padding: 8px 15px; cursor: pointer; }
                    &lt;/style&gt;
                &lt;/head&gt;
                &lt;body&gt;
                    &lt;h1&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>ans<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">!!!&lt;/h1&gt;
                    &lt;hr&gt;
                    &lt;button onClick="window.close();"&gt;Закрыть&lt;/button&gt;
                &lt;/body&gt;
                &lt;/html&gt;
            `</span></span><span class="token punctuation">;</span>

            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>htmlContent<span class="token punctuation">)</span><span class="token punctuation">;</span>
            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Проверка таблицы умножения<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Отметьте правильные утверждения:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>checkbox<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c1<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c1<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>2*2=4<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c1<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>2*2=4<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>checkbox<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c2<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c2<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>2*5=30<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c2<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>2*5=30<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>checkbox<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c3<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c3<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>6*8=48<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>c3<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>6*8=48<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Проверить<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>checkAll();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab5_checkbox_new_window.html</code>.</li>
<li>Откройте файл в браузере.</li>
<li>Попробуйте разные комбинации отметок и нажмите “Проверить”. Результат появится в новом окне.</li>
</ol>
<hr>
<p><strong>Пример 3 (стр. 41) - Проверка выбора радиокнопки</strong></p>
<p>Демонстрирует, как проверить, какая радиокнопка выбрана, используя свойство <code>checked</code>.</p>
<p><strong>Код для Примера 3:</strong></p>
<p><strong>Файл: <code>lab5_radio_check.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Проверка радиокнопок<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">validate</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> resultMessage <span class="token operator">=</span> <span class="token string">"неверно"</span><span class="token punctuation">;</span> <span class="token comment">// Изначально предполагаем ошибку</span>

            <span class="token comment">// Получаем ссылки на каждую радиокнопку по их id</span>
            <span class="token keyword">var</span> k1 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'k1'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// целое число</span>
            <span class="token keyword">var</span> k2 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'k2'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// строку</span>
            <span class="token keyword">var</span> k3 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'k3'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// вещественное число</span>

            <span class="token comment">// Правильный ответ: prompt() возвращает строку, поэтому k2 должна быть выбрана</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>k2<span class="token punctuation">.</span>checked<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                resultMessage <span class="token operator">=</span> <span class="token string">"верно"</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token function">alert</span><span class="token punctuation">(</span>resultMessage<span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Что возвращает метод prompt() объекта window?<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h3</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>radio<span class="token punctuation">'</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>k1<span class="token punctuation">'</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>v<span class="token punctuation">'</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>integer<span class="token punctuation">'</span></span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>k1<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>целое число<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>radio<span class="token punctuation">'</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>k2<span class="token punctuation">'</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>v<span class="token punctuation">'</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>string<span class="token punctuation">'</span></span> <span class="token attr-name">checked</span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>k2<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>строку<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>radio<span class="token punctuation">'</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>k3<span class="token punctuation">'</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>v<span class="token punctuation">'</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>float<span class="token punctuation">'</span></span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>k3<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>вещественное число<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h3</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Проверить<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>validate();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab5_radio_check.html</code>.</li>
<li>Откройте файл в браузере.</li>
<li>Попробуйте выбрать разные радиокнопки и нажмите “Проверить”. Убедитесь, что “верно” появится только при выборе “строку”.</li>
</ol>
<hr>
<p><strong>Пример 4 (стр. 42-43) - Выравнивание текста в новом окне (Radio Buttons)</strong></p>
<p>Запрашивает текст и выбранное выравнивание (лево, право, центр) с помощью радиокнопок. Затем открывает новое окно и выводит в нем введенный текст с соответствующим выравниванием.</p>
<p><strong>Код для Примера 4:</strong></p>
<p><strong>Файл: <code>lab5_radio_alignment.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Выравнивание текста<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">h1, h2, h3 </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">label </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">300</span>px<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="radio"]</span> </span><span class="token punctuation">{</span> <span class="token property">margin-right</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">br </span><span class="token punctuation">{</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">400</span>px<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f9f9f9</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">validate</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Получаем текст из текстового поля</span>
            <span class="token keyword">var</span> txInput <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'tx'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> textt <span class="token operator">=</span> txInput<span class="token punctuation">.</span>value<span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>textt<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">===</span> <span class="token string">""</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Пожалуйста, введите текст для отображения."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Получаем ссылки на радиокнопки</span>
            <span class="token keyword">var</span> p1 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'k1'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// по левой стороне</span>
            <span class="token keyword">var</span> p2 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'k2'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// по правой стороне</span>
            <span class="token keyword">var</span> p3 <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'k3'</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// по центру</span>

            <span class="token keyword">var</span> alignment <span class="token operator">=</span> <span class="token string">'left'</span><span class="token punctuation">;</span> <span class="token comment">// Выравнивание по умолчанию</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>p1<span class="token punctuation">.</span>checked<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                alignment <span class="token operator">=</span> <span class="token string">'left'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>p2<span class="token punctuation">.</span>checked<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                alignment <span class="token operator">=</span> <span class="token string">'right'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>p3<span class="token punctuation">.</span>checked<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                alignment <span class="token operator">=</span> <span class="token string">'center'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Открываем новое окно</span>
            <span class="token keyword">var</span> win <span class="token operator">=</span> window<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"width=400,height=200"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>win<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Не удалось открыть новое окно."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Формируем HTML-контент для нового окна</span>
            <span class="token keyword">var</span> htmlContent <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
                &lt;!DOCTYPE html&gt;
                &lt;html&gt;
                &lt;head&gt;
                    &lt;title&gt;Результат выравнивания&lt;/title&gt;
                    &lt;style&gt;
                        h2 { text-align: </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>alignment<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">; color: blue; }
                        body { font-family: Arial, sans-serif; }
                        button { margin-top: 20px; padding: 8px 15px; cursor: pointer; }
                    &lt;/style&gt;
                &lt;/head&gt;
                &lt;body&gt;
                    &lt;h2&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>textt<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/h2&gt;
                    &lt;button onClick="window.close();"&gt;Закрыть&lt;/button&gt;
                &lt;/body&gt;
                &lt;/html&gt;
            `</span></span><span class="token punctuation">;</span>

            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>htmlContent<span class="token punctuation">)</span><span class="token punctuation">;</span>
            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Выравнивание текста<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h3</span><span class="token punctuation">&gt;</span></span>Введите текст<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h3</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>tx<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>tx<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Привет!<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>

        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h3</span><span class="token punctuation">&gt;</span></span>Выберите выравнивание<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h3</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>radio<span class="token punctuation">'</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>k1<span class="token punctuation">'</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>v<span class="token punctuation">'</span></span> <span class="token attr-name">checked</span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>k1<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>по левой стороне<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>radio<span class="token punctuation">'</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>k2<span class="token punctuation">'</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>v<span class="token punctuation">'</span></span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>k2<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>по правой стороне<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>radio<span class="token punctuation">'</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>k3<span class="token punctuation">'</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>v<span class="token punctuation">'</span></span><span class="token punctuation">&gt;</span></span> <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>k3<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>по центру<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Показать<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>validate();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab5_radio_alignment.html</code>.</li>
<li>Откройте файл в браузере.</li>
<li>Введите текст, выберите выравнивание и нажмите “Показать”. Убедитесь, что текст в новом окне выравнивается согласно вашему выбору.</li>
</ol>
<hr>
<p><strong>Пример 5 (стр. 44) - Выбор картинки из списка (Select/Option)</strong></p>
<p>Демонстрирует, как получить выбранную опцию из выпадающего списка (<code>&lt;select&gt;</code>) и использовать ее для отображения картинки в новом окне.</p>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>2.GIF</code> (или любое другое изображение - назовите, например, <code>krokodil.gif</code>)</li>
<li><code>200.png</code> (или другое изображение, например, <code>ptichka.png</code>)</li>
<li><code>ALLIGATO.gif</code> (или другое изображение, например, <code>fish.png</code>)</li>
</ul>
<p><strong>Код для Примера 5:</strong></p>
<p><strong>Файл: <code>lab5_select_image.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Выбор картинки из списка<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">GO</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Получаем ссылку на элемент &lt;select&gt;</span>
            <span class="token keyword">var</span> selectElement <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'imageSelect'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Получаем выбранный элемент &lt;option&gt;</span>
            <span class="token keyword">var</span> selectedOption <span class="token operator">=</span> selectElement<span class="token punctuation">.</span>options<span class="token punctuation">[</span>selectElement<span class="token punctuation">.</span>selectedIndex<span class="token punctuation">]</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> titleText <span class="token operator">=</span> selectedOption<span class="token punctuation">.</span>text<span class="token punctuation">;</span> <span class="token comment">// Текст выбранной опции</span>
            <span class="token keyword">var</span> imageSrc <span class="token operator">=</span> selectedOption<span class="token punctuation">.</span>value<span class="token punctuation">;</span> <span class="token comment">// Значение (value) выбранной опции, здесь это путь к картинке</span>

            <span class="token comment">// Проверяем, выбрана ли какая-то опция</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>imageSrc<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Пожалуйста, выберите изображение из списка."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Открываем новое окно</span>
            <span class="token keyword">var</span> win <span class="token operator">=</span> window<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"width=400,height=300"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>win<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Не удалось открыть новое окно."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> htmlContent <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
                &lt;!DOCTYPE html&gt;
                &lt;html&gt;
                &lt;head&gt;
                    &lt;title&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>titleText<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/title&gt;
                    &lt;style&gt;
                        body { font-family: Arial, sans-serif; text-align: center; margin-top: 20px; background-color: #f0f8ff; }
                        h2 { color: #333; }
                        img { max-width: 90%; height: auto; display: block; margin: 10px auto; border: 1px solid #ccc; }
                        button { margin-top: 20px; padding: 8px 15px; cursor: pointer; }
                    &lt;/style&gt;
                &lt;/head&gt;
                &lt;body&gt;
                    &lt;h2&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>titleText<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/h2&gt;
                    &lt;img src="</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>imageSrc<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">" alt="</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>titleText<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">"&gt;
                    &lt;button onClick="window.close();"&gt;Закрыть&lt;/button&gt;
                &lt;/body&gt;
                &lt;/html&gt;
            `</span></span><span class="token punctuation">;</span>

            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>htmlContent<span class="token punctuation">)</span><span class="token punctuation">;</span>
            win<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Выбор картинки из списка<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h3</span><span class="token punctuation">&gt;</span></span>Выберите картинку<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h3</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>select</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>imageSelect<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token comment">&lt;!-- value каждого option будет путем к изображению. text - его описание --&gt;</span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>option</span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>-- Выберите --<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>option</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>option</span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>200.png<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Птичка<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>option</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>option</span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>fish.png<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Рыбка<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>option</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>option</span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>krokodil.gif<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Крокодил<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>option</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>select</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Показать<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>GO();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Создайте новую папку, например, <code>lab5_select_images</code>.</li>
<li>Соберите три изображения (или создайте заглушки размером 200x200 пикселей) и назовите их: <code>200.png</code> (для птички), <code>fish.png</code> (для рыбки), <code>krokodil.gif</code> (для крокодила). Поместите их в папку <code>lab5_select_images</code>.</li>
<li>В той же папке создайте файл <code>lab5_select_image.html</code> и скопируйте в него предоставленный код.</li>
<li>Откройте файл в браузере.</li>
<li>Выберите опцию из выпадающего списка и нажмите “Показать”. Выбранная картинка должна появиться в новом окне.</li>
</ol>
<hr>
<p><strong>Задание 1 (стр. 45) - Вариант 1 (Страничка по заказу)</strong></p>
<p><strong>Задача:</strong> Создать HTML-приложение, которое имитирует форму заказа. Пользователь выбирает заголовок, картинку (радиокнопка), подпись, цвета фона и текста (радиокнопки). По нажатию кнопки “Показать” приложение должно открыть новое окно и показать в нем заказанные картинки с короткими подписями. Новое окно должно создаваться “на лету” с использованием информации, которую ввел пользователь.</p>
<p><strong>Решено:</strong> Комбинация предыдущих техник: <code>getElementById()</code>, <code>value</code>, <code>checked</code> для сбора данных из радиокнопок/текстовых полей, <code>window.open()</code>, <code>document.write()</code> для формирования нового окна.</p>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>dog.jpg</code></li>
<li><code>bigdaisy.jpg</code></li>
<li><code>flower.jpg</code><br>
(поместите их в папку с файлом HTML)</li>
</ul>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab5_task1_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура с формой заказа:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Страничка по заказу<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f0f0</span><span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">justify-content</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span> flex-start<span class="token punctuation">;</span> <span class="token property">min-height</span><span class="token punctuation">:</span> <span class="token number">100</span>vh<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px <span class="token number">0</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.container</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f7e0f2</span><span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#e0c8d8</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">25</span>px<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">box-shadow</span><span class="token punctuation">:</span> <span class="token number">0</span> <span class="token number">4</span>px <span class="token number">8</span>px <span class="token function">rgba</span><span class="token punctuation">(</span><span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">550</span>px<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#8e44ad</span><span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form div </span><span class="token punctuation">{</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form label </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> inline-block<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100</span>px<span class="token punctuation">;</span> <span class="token property">font-weight</span><span class="token punctuation">:</span> bold<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token function">calc</span><span class="token punctuation">(</span><span class="token number">100%</span> - <span class="token number">110</span>px<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form div<span class="token class">.radio-group</span> label </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> auto<span class="token punctuation">;</span> <span class="token property">margin-right</span><span class="token punctuation">:</span> <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token property">font-weight</span><span class="token punctuation">:</span> normal<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form div<span class="token class">.radio-group</span> input<span class="token attribute">[type="radio"]</span> </span><span class="token punctuation">{</span> <span class="token property">margin-right</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form button </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#showButton</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#8e44ad</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#showButton</span><span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#6c3580</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#resetButton</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#b0b0b0</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">margin-left</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#resetButton</span><span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#909090</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">showOrder</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// 1. Получение данных из формы</span>
            <span class="token keyword">var</span> title <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'headerInput'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>
            <span class="token keyword">var</span> caption <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'captionInput'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>

            <span class="token keyword">var</span> imageSrc <span class="token operator">=</span> <span class="token string">''</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'imgDog'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> imageSrc <span class="token operator">=</span> <span class="token string">'dog.jpg'</span><span class="token punctuation">;</span>
            <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'imgDaisy'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> imageSrc <span class="token operator">=</span> <span class="token string">'bigdaisy.jpg'</span><span class="token punctuation">;</span>
            <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'imgFlower'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> imageSrc <span class="token operator">=</span> <span class="token string">'flower.jpg'</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> bgColor <span class="token operator">=</span> <span class="token string">''</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'bgGreen'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> bgColor <span class="token operator">=</span> <span class="token string">'lightgreen'</span><span class="token punctuation">;</span>
            <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'bgYellow'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> bgColor <span class="token operator">=</span> <span class="token string">'yellow'</span><span class="token punctuation">;</span>
            <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'bgBlue'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> bgColor <span class="token operator">=</span> <span class="token string">'skyblue'</span><span class="token punctuation">;</span>

            <span class="token keyword">var</span> textColor <span class="token operator">=</span> <span class="token string">''</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'textBlack'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> textColor <span class="token operator">=</span> <span class="token string">'black'</span><span class="token punctuation">;</span>
            <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'textRed'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> textColor <span class="token operator">=</span> <span class="token string">'red'</span><span class="token punctuation">;</span>
            <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'textWhite'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> textColor <span class="token operator">=</span> <span class="token string">'white'</span><span class="token punctuation">;</span>

            <span class="token comment">// Валидация ввода</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>title<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token operator">!</span>caption<span class="token punctuation">.</span><span class="token function">trim</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token operator">!</span>imageSrc <span class="token operator">||</span> <span class="token operator">!</span>bgColor <span class="token operator">||</span> <span class="token operator">!</span>textColor<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">'Пожалуйста, заполните все поля!'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// 2. Формирование HTML для нового окна</span>
            <span class="token keyword">var</span> newWindowHtml <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
                &lt;!DOCTYPE html&gt;
                &lt;html&gt;
                &lt;head&gt;
                    &lt;title&gt;Ваш заказ&lt;/title&gt;
                    &lt;style&gt;
                        body {
                            font-family: Arial, sans-serif;
                            background-color: </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>bgColor<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">;
                            margin: 20px;
                            text-align: center;
                        }
                        h1 { color: </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>textColor<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">; }
                        p { font-size: 1.1em; color: </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>textColor<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">; }
                        img { max-width: 80%; height: auto; border: 2px solid </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>textColor<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">; margin-top: 20px; }
                        button { margin-top: 30px; padding: 10px 20px; background-color: #6c757d; color: white; border: none; cursor: pointer; border-radius: 5px; }
                        button:hover { background-color: #5a6268; }
                    &lt;/style&gt;
                &lt;/head&gt;
                &lt;body&gt;
                    &lt;h1&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>title<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/h1&gt;
                    &lt;img src="</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>imageSrc<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">" alt="Заказанная картинка"&gt;
                    &lt;p&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>caption<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/p&gt;
                    &lt;button onClick="window.close();"&gt;Закрыть&lt;/button&gt;
                &lt;/body&gt;
                &lt;/html&gt;
            `</span></span><span class="token punctuation">;</span>

            <span class="token comment">// 3. Открытие и запись в новое окно</span>
            <span class="token keyword">var</span> newWin <span class="token operator">=</span> window<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"_blank"</span><span class="token punctuation">,</span> <span class="token string">"width=600,height=500,scrollbars=yes,resizable=yes"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>newWin<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">'Не удалось открыть новое окно. Возможно, блокировщик всплывающих окон.'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            newWin<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            newWin<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>newWindowHtml<span class="token punctuation">)</span><span class="token punctuation">;</span>
            newWin<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>

        <span class="token keyword">function</span> <span class="token function">clearForm</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'headerInput'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">''</span><span class="token punctuation">;</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'captionInput'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">''</span><span class="token punctuation">;</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'imgDog'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span> <span class="token comment">// Сброс изображения на первое по умолчанию</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'bgGreen'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span> <span class="token comment">// Сброс фона</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'textBlack'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span> <span class="token comment">// Сброс цвета текста</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span> <span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Страничка по заказу<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>headerInput<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Заголовок:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>headerInput<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Собака друг человека!<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>captionInput<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Подпись:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>captionInput<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Я тоже завел себе верного пса, собаку которая ру<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span><span class="token punctuation">&gt;</span></span>Картинка:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio-group<span class="token punctuation">"</span></span><span class="token style-attr language-css"><span class="token attr-name"> <span class="token attr-name">style</span></span><span class="token punctuation">="</span><span class="token attr-value"><span class="token property">display</span><span class="token punctuation">:</span>inline-block<span class="token punctuation">;</span></span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>imgDog<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>image<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>dog.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">checked</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>imgDog<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Собака<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>imgDaisy<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>image<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bigdaisy.jpg<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>imgDaisy<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Одинокий цветок<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>imgFlower<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>image<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>flower.jpg<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>imgFlower<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Букет<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span><span class="token punctuation">&gt;</span></span>Цвет фона:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio-group<span class="token punctuation">"</span></span><span class="token style-attr language-css"><span class="token attr-name"> <span class="token attr-name">style</span></span><span class="token punctuation">="</span><span class="token attr-value"><span class="token property">display</span><span class="token punctuation">:</span>inline-block<span class="token punctuation">;</span></span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bgGreen<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bgColor<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>lightgreen<span class="token punctuation">"</span></span> <span class="token attr-name">checked</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bgGreen<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>зеленый<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bgYellow<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bgColor<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>yellow<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bgYellow<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>желтый<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bgBlue<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bgColor<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>skyblue<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bgBlue<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>синий<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span><span class="token punctuation">&gt;</span></span>Цвет текста:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio-group<span class="token punctuation">"</span></span><span class="token style-attr language-css"><span class="token attr-name"> <span class="token attr-name">style</span></span><span class="token punctuation">="</span><span class="token attr-value"><span class="token property">display</span><span class="token punctuation">:</span>inline-block<span class="token punctuation">;</span></span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>textBlack<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>textColor<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>black<span class="token punctuation">"</span></span> <span class="token attr-name">checked</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>textBlack<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>черный<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>textRed<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>textColor<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>red<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>textRed<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>красный<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>textWhite<span class="token punctuation">"</span></span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>textColor<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>white<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>textWhite<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>белый<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showButton<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showOrder();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Показать<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>resetButton<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>clearForm();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Сброс<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображения:</strong> Скачайте или создайте изображения <code>dog.jpg</code>, <code>bigdaisy.jpg</code>, <code>flower.jpg</code> и поместите их в ту же папку.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab5_task1_var1.html</code> в браузере. Заполните форму, выберите опции и нажмите “Показать”.</p>
</li>
</ol>
<hr>
<p><strong>Задание 2 (стр. 46) - Вариант 2 (Страничка по заказу - Художники)</strong></p>
<p><strong>Задача:</strong> Создать HTML-приложение, схожее с Заданием 1, но с данными о художнике, его подписью и опциями декорации текста (<code>italic</code>, <code>underline</code>, <code>bold</code>).</p>
<p><strong>Решено:</strong> Использование <code>&lt;select&gt;</code> для выбора художника, <code>value</code> для хранения его данных, и флажков для стилей текста.</p>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>footer.jpg</code>, <code>222.jpg</code>, <code>bg16.jpg</code> (и др. для художников: <code>Tropyinin.jpg</code>, <code>Repin.jpg</code>, <code>Aivazovsky.jpg</code>) - поместите их в папку с файлом HTML. (В примере будет использоваться только один файл.)</li>
</ul>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab5_task2_var2.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура с формой заказа художника:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Страничка по заказу - Художник<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f0f0</span><span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">justify-content</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span>flex-start<span class="token punctuation">;</span> <span class="token property">min-height</span><span class="token punctuation">:</span> <span class="token number">100</span>vh<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px <span class="token number">0</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.container</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#e0faff</span><span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#c0e0e8</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">25</span>px<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">box-shadow</span><span class="token punctuation">:</span> <span class="token number">0</span> <span class="token number">4</span>px <span class="token number">8</span>px <span class="token function">rgba</span><span class="token punctuation">(</span><span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">550</span>px<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#4682b4</span><span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form div </span><span class="token punctuation">{</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form label </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> inline-block<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">150</span>px<span class="token punctuation">;</span> <span class="token property">font-weight</span><span class="token punctuation">:</span> bold<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form input<span class="token attribute">[type="text"]</span>, form select </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token function">calc</span><span class="token punctuation">(</span><span class="token number">100%</span> - <span class="token number">160</span>px<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">4</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form div<span class="token class">.radio-group</span> label </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> auto<span class="token punctuation">;</span> <span class="token property">margin-right</span><span class="token punctuation">:</span> <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token property">font-weight</span><span class="token punctuation">:</span> normal<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form div<span class="token class">.radio-group</span> input<span class="token attribute">[type="checkbox"]</span> </span><span class="token punctuation">{</span> <span class="token property">margin-right</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form button </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">15</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#showButton</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#4682b4</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#showButton</span><span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#36678c</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#resetButton</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#b0b0b0</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token property">margin-left</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#resetButton</span><span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#909090</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Данные о художниках (путь к портрету, подпись)</span>
        <span class="token keyword">var</span> artists <span class="token operator">=</span> <span class="token punctuation">{</span>
            <span class="token string">"tropyinin"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span> 
                name<span class="token punctuation">:</span> <span class="token string">"Тропинин"</span><span class="token punctuation">,</span> 
                img<span class="token punctuation">:</span> <span class="token string">"tropyinin.jpg"</span><span class="token punctuation">,</span> 
                bio<span class="token punctuation">:</span> <span class="token string">"Родился 19 марта 1776 в селе Карпово Новгородской губернии"</span> 
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token string">"repin"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span> 
                name<span class="token punctuation">:</span> <span class="token string">"Репин"</span><span class="token punctuation">,</span> 
                img<span class="token punctuation">:</span> <span class="token string">"repin.jpg"</span><span class="token punctuation">,</span> 
                bio<span class="token punctuation">:</span> <span class="token string">"Родился 5 августа 1844 года в городе Чугуеве"</span> 
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token string">"aivazovsky"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span> 
                name<span class="token punctuation">:</span> <span class="token string">"Айвазовский"</span><span class="token punctuation">,</span> 
                img<span class="token punctuation">:</span> <span class="token string">"aivazovsky.jpg"</span><span class="token punctuation">,</span> 
                bio<span class="token punctuation">:</span> <span class="token string">"Родился 17 июля 1817 года в Феодосии, Таврическая губерния"</span> 
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span><span class="token punctuation">;</span>

        <span class="token keyword">function</span> <span class="token function">updateCaption</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> select <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'artistSelect'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> selectedArtistId <span class="token operator">=</span> select<span class="token punctuation">.</span>value<span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>selectedArtistId <span class="token operator">&amp;&amp;</span> artists<span class="token punctuation">[</span>selectedArtistId<span class="token punctuation">]</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'captionInput'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> artists<span class="token punctuation">[</span>selectedArtistId<span class="token punctuation">]</span><span class="token punctuation">.</span>bio<span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'captionInput'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">''</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>

        <span class="token keyword">function</span> <span class="token function">showOrder</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> select <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'artistSelect'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> selectedArtistId <span class="token operator">=</span> select<span class="token punctuation">.</span>value<span class="token punctuation">;</span>
            
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>selectedArtistId <span class="token operator">||</span> <span class="token operator">!</span>artists<span class="token punctuation">[</span>selectedArtistId<span class="token punctuation">]</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">'Пожалуйста, выберите художника!'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>

            <span class="token keyword">var</span> artist <span class="token operator">=</span> artists<span class="token punctuation">[</span>selectedArtistId<span class="token punctuation">]</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> caption <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'captionInput'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value<span class="token punctuation">;</span>

            <span class="token comment">// Сбор стилей текста</span>
            <span class="token keyword">var</span> textStyle <span class="token operator">=</span> <span class="token string">''</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'italic'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> textStyle <span class="token operator">+=</span> <span class="token string">'font-style: italic;'</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'underline'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> textStyle <span class="token operator">+=</span> <span class="token string">'text-decoration: underline;'</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'bold'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked<span class="token punctuation">)</span> textStyle <span class="token operator">+=</span> <span class="token string">'font-weight: bold;'</span><span class="token punctuation">;</span>

            <span class="token comment">// Формирование HTML для нового окна</span>
            <span class="token keyword">var</span> newWindowHtml <span class="token operator">=</span> <span class="token template-string"><span class="token string">`
                &lt;!DOCTYPE html&gt;
                &lt;html&gt;
                &lt;head&gt;
                    &lt;title&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>artist<span class="token punctuation">.</span>name<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/title&gt;
                    &lt;style&gt;
                        body {
                            font-family: Arial, sans-serif;
                            background-color: #fdf5e6; /* Легкий бежевый фон */
                            margin: 20px;
                            text-align: center;
                        }
                        h1 { color: #8b4513; }
                        p { font-size: 1.1em; color: #555; </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>textStyle<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> }
                        img { max-width: 80%; height: auto; border: 2px solid #8b4513; margin-top: 20px; }
                        button { margin-top: 30px; padding: 10px 20px; background-color: #6c757d; color: white; border: none; cursor: pointer; border-radius: 5px; }
                        button:hover { background-color: #5a6268; }
                    &lt;/style&gt;
                &lt;/head&gt;
                &lt;body&gt;
                    &lt;h1&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>artist<span class="token punctuation">.</span>name<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/h1&gt;
                    &lt;img src="</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>artist<span class="token punctuation">.</span>img<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">" alt="</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>artist<span class="token punctuation">.</span>name<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">"&gt;
                    &lt;p&gt;</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>caption<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">&lt;/p&gt;
                    &lt;button onClick="window.close();"&gt;Закрыть&lt;/button&gt;
                &lt;/body&gt;
                &lt;/html&gt;
            `</span></span><span class="token punctuation">;</span>

            <span class="token comment">// Открытие и запись в новое окно</span>
            <span class="token keyword">var</span> newWin <span class="token operator">=</span> window<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span> <span class="token string">"_blank"</span><span class="token punctuation">,</span> <span class="token string">"width=600,height=600,scrollbars=yes,resizable=yes"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>newWin<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">'Не удалось открыть новое окно. Возможно, блокировщик всплывающих окон.'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            newWin<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">open</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            newWin<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span>newWindowHtml<span class="token punctuation">)</span><span class="token punctuation">;</span>
            newWin<span class="token punctuation">.</span>document<span class="token punctuation">.</span><span class="token function">close</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>

        <span class="token keyword">function</span> <span class="token function">clearForm</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'artistSelect'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">''</span><span class="token punctuation">;</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'captionInput'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">''</span><span class="token punctuation">;</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'italic'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'underline'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'bold'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>checked <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span> <span class="token attr-name">onLoad</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>updateCaption();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Страничка по заказу<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>artistSelect<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Художник:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>select</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>artistSelect<span class="token punctuation">"</span></span> <span class="token attr-name">onChange</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>updateCaption();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>option</span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>-- Выберите художника --<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>option</span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>option</span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>tropyinin<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Тропинин<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>option</span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>option</span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>repin<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Репин<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>option</span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>option</span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>aivazovsky<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Айвазовский<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>option</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>select</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>captionInput<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Подпись:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>captionInput<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span><span class="token punctuation">&gt;</span></span>Декорирование текста:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>radio-group<span class="token punctuation">"</span></span><span class="token style-attr language-css"><span class="token attr-name"> <span class="token attr-name">style</span></span><span class="token punctuation">="</span><span class="token attr-value"><span class="token property">display</span><span class="token punctuation">:</span>inline-block<span class="token punctuation">;</span></span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>checkbox<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>italic<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>italic<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>курсив<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>checkbox<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>underline<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>underline<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>подчеркивание<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>checkbox<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bold<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>label</span> <span class="token attr-name">for</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bold<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>жирный<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>label</span><span class="token punctuation">&gt;</span></span>
                <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showButton<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showOrder();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Показать<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>resetButton<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>clearForm();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Сброс<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображения:</strong> Скачайте или создайте изображения <code>tropyinin.jpg</code>, <code>repin.jpg</code>, <code>aivazovsky.jpg</code> (или используйте любые другие портреты) и поместите их в ту же папку.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab5_task2_var2.html</code> в браузере. Выберите художника, настройте стили и нажмите “Показать”.</p>
</li>
</ol>
<hr>
<p>Это завершает <strong>ЛАБОРАТОРНУЮ РАБОТУ № 5</strong>.</p>
<p>Отлично! Переходим к <strong>ЛАБОРАТОРНОЙ РАБОТЕ № 6: Объект Image</strong>.</p>
<hr>
<h3 id="лабораторная-работа-№-6-объект-image"><strong>ЛАБОРАТОРНАЯ РАБОТА № 6: Объект Image</strong></h3>
<p><strong>Цель:</strong> Изучить работу с изображениями (<code>&lt;img&gt;</code> элементами) в JavaScript. Основное внимание будет уделено свойству <code>src</code> объекта <code>Image</code> и обработке событий мыши (<code>onMouseOver</code>, <code>onMouseOut</code>) для создания интерактивных эффектов, таких как изменение изображения при наведении курсора и создание слайд-шоу.</p>
<p><strong>Общее описание:</strong></p>
<ul>
<li><strong>Объект <code>Image</code>:</strong> Все <code>&lt;img&gt;</code> элементы в HTML-додокументе являются экземплярами объекта <code>Image</code>. Ключевое свойство <code>Image</code> - <code>src</code> (источник изображения). Изменяя это свойство, можно динамически менять отображаемое изображение.</li>
<li><strong>События мыши:</strong>
<ul>
<li><code>onMouseOver</code>: Происходит, когда курсор мыши наводится на элемент.</li>
<li><code>onMouseOut</code>: Происходит, когда курсор мыши уходит с элемента.</li>
</ul>
</li>
<li><strong>Таймеры:</strong>
<ul>
<li><code>setTimeout()</code>: Выполняет функцию или фрагмент кода один раз после указанной задержки.</li>
<li><code>setInterval()</code>: Выполняет функцию или фрагмент кода многократно через указанные интервалы.</li>
</ul>
</li>
</ul>
<hr>
<p><strong>Примеры из пособия (стр. 48-51) и их выполнение:</strong></p>
<p><strong>Пример 1 (стр. 48) - <code>onMouseOver</code> и <code>onMouseOut</code> для смены изображения</strong></p>
<p>Демонстрирует, как менять изображение при наведении курсора мыши (<code>onMouseOver</code>) и возвращать его в исходное состояние при уходе курсора (<code>onMouseOut</code>).</p>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>bigdaisy.jpg</code> (или другое изображение, исходное)</li>
<li><code>flower.jpg</code> (или другое изображение, которое появится при наведении)</li>
</ul>
<p><strong>Код для Примера 1:</strong></p>
<p><strong>Файл: <code>lab6_mouseover_image.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Смена изображения по MouseOver/Out<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#dfd8c5</span><span class="token punctuation">;</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">img </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">274</span>px<span class="token punctuation">;</span> <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">233</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">2</span>px solid <span class="token hexcode">#555</span><span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token punctuation">}</span> <span class="token comment">/* Размеры из пособия */</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#333</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">p </span><span class="token punctuation">{</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#666</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">doEvent</span><span class="token punctuation">(</span>type<span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Получаем ссылку на изображение по id 'pic'</span>
            <span class="token keyword">var</span> cv <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'pic'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Если type == true (значит onMouseOver)</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>type<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                cv<span class="token punctuation">.</span>src <span class="token operator">=</span> <span class="token string">"flower.jpg"</span><span class="token punctuation">;</span> <span class="token comment">// Меняем на flower.jpg</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span> <span class="token comment">// Если type == false (значит onMouseOut)</span>
                cv<span class="token punctuation">.</span>src <span class="token operator">=</span> <span class="token string">"bigdaisy.jpg"</span><span class="token punctuation">;</span> <span class="token comment">// Возвращаем bigdaisy.jpg</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>События MouseOver и MouseOut<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Переведи мышиный курсор на цветок!<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>pic<span class="token punctuation">'</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bigdaisy.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Цветок<span class="token punctuation">"</span></span>
         <span class="token attr-name">onMouseOver</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>doEvent(true);<span class="token punctuation">"</span></span>
         <span class="token attr-name">onMouseOut</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>doEvent(false);<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Создайте новую папку, например, <code>lab6_images</code>.</li>
<li>Поместите изображения <code>bigdaisy.jpg</code> (или любое другое исходное) и <code>flower.jpg</code> (или любое другое для эффекта) в эту папку.</li>
<li>Создайте файл <code>lab6_mouseover_image.html</code> и скопируйте в него предоставленный код.</li>
<li>Откройте файл в браузере. Наведите курсор на изображение и убедитесь, что оно меняется. Уберите курсор, и оно должно вернуться.</li>
</ol>
<hr>
<p><strong>Пример 2 (стр. 49-50) - <code>onMouseOver</code> и <code>onMouseOut</code> для подсказок (Tooltip)</strong></p>
<p>Демонстрирует, как показывать текстовые подсказки в текстовом поле при наведении на кнопки, и скрывать их при уходе с кнопок.</p>
<p><strong>Код для Примера 2:</strong></p>
<p><strong>Файл: <code>lab6_tooltip_buttons.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Подсказки к кнопкам<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#dfd8c5</span><span class="token punctuation">;</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">form </span><span class="token punctuation">{</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">30</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="button"]</span> </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="text"]</span> </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">400</span>px<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">1</span>em<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Массив подсказок:</span>
        <span class="token comment">// index 0: пустая строка (для скрытия подсказки)</span>
        <span class="token comment">// index 1: Выключение компьютера</span>
        <span class="token comment">// index 2: Удаление файлов с системного диска</span>
        <span class="token comment">// index 3: Форматирование винчестера</span>
        <span class="token keyword">var</span> mess <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Array</span><span class="token punctuation">(</span><span class="token string">""</span><span class="token punctuation">,</span>
                             <span class="token string">"Выключение компьютера"</span><span class="token punctuation">,</span>
                             <span class="token string">"Удаление файлов с системного диска"</span><span class="token punctuation">,</span>
                             <span class="token string">"Форматирование винчестера"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">function</span> <span class="token function">doEvent</span><span class="token punctuation">(</span>num<span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Получаем ссылку на текстовое поле для подсказок по id 'info'</span>
            <span class="token keyword">var</span> cv <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'info'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Присваиваем значение из массива подсказок соответствующему индексу 'num'</span>
            cv<span class="token punctuation">.</span>value <span class="token operator">=</span> mess<span class="token punctuation">[</span>num<span class="token punctuation">]</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>onMouseOver и onMouseOut<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Перед тем, как нажать кнопку, хорошо подумай!<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>1 <span class="token punctuation">"</span></span>
               <span class="token attr-name">onMouseOver</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>doEvent(1);<span class="token punctuation">"</span></span>
               <span class="token attr-name">onMouseOut</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>doEvent(0);<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>2 <span class="token punctuation">"</span></span>
               <span class="token attr-name">onMouseOver</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>doEvent(2);<span class="token punctuation">"</span></span>
               <span class="token attr-name">onMouseOut</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>doEvent(0);<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>3 <span class="token punctuation">"</span></span>
               <span class="token attr-name">onMouseOver</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>doEvent(3);<span class="token punctuation">"</span></span>
               <span class="token attr-name">onMouseOut</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>doEvent(0);<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">name</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>info<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>info<span class="token punctuation">'</span></span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span> <span class="token attr-name">size</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>50<span class="token punctuation">"</span></span> <span class="token attr-name">readonly</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab6_tooltip_buttons.html</code>.</li>
<li>Откройте файл в браузере. Наведите курсор на кнопки и убедитесь, что подсказки появляются в текстовом поле. Уберите курсор, и подсказка должна исчезнуть.</li>
</ol>
<hr>
<p><strong>Пример 3 (стр. 51) - Слайд-шоу с <code>setTimeout()</code></strong></p>
<p>Демонстрирует создание автоматического слайд-шоу, где изображения меняются через определенные интервалы с использованием <code>setTimeout()</code>.</p>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>7.png</code>, <code>8.png</code>, <code>9.png</code>, <code>6.png</code> (или любые другие изображения для слайд-шоу)</li>
</ul>
<p><strong>Код для Примера 3:</strong></p>
<p><strong>Файл: <code>lab6_slideshow_auto.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Автоматическое слайд-шоу<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f8ff</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">img </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">400</span>px<span class="token punctuation">;</span> <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">300</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">2</span>px solid <span class="token hexcode">#555</span><span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#333</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="button"]</span> </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Текущий индекс изображения в массиве</span>
        <span class="token keyword">var</span> i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
        <span class="token comment">// Массив картинок (пути к файлам)</span>
        <span class="token keyword">var</span> ris <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Array</span><span class="token punctuation">(</span><span class="token string">'7.png'</span><span class="token punctuation">,</span> <span class="token string">'8.png'</span><span class="token punctuation">,</span> <span class="token string">'9.png'</span><span class="token punctuation">,</span> <span class="token string">'6.png'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">function</span> <span class="token function">slideShow</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Получаем ссылку на изображение по id 'slide'</span>
            <span class="token keyword">var</span> r <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'slide'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Проверяем, не вышел ли счетчик за пределы массива</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>i <span class="token operator">&gt;=</span> ris<span class="token punctuation">.</span>length<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Если вышел, обнуляем счетчик (начинаем сначала)</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Меняем свойство src этого объекта на элемент из массива</span>
            r<span class="token punctuation">.</span>src <span class="token operator">=</span> ris<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">;</span>

            i<span class="token operator">++</span><span class="token punctuation">;</span> <span class="token comment">// Увеличиваем счетчик для следующего изображения</span>

            <span class="token comment">// Вызываем эту же функцию через 1500 мс (1.5 секунды)</span>
            <span class="token comment">// Это создает автоматическую смену изображений</span>
            <span class="token function">setTimeout</span><span class="token punctuation">(</span>slideShow<span class="token punctuation">,</span> <span class="token number">1500</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>

        <span class="token comment">// Запускаем слайд-шоу при загрузке страницы</span>
        <span class="token comment">// Можно вызывать по onLoad на body, либо через кнопку как в примере.</span>
        <span class="token comment">// Здесь вызовем по нажатию кнопки для соответствия примеру пособия.</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Слайд-шоу<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>slide<span class="token punctuation">'</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Слайд-шоу<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
    <span class="token comment">&lt;!-- Кнопка для запуска слайд-шоу --&gt;</span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Начать<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>slideShow();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Создайте новую папку, например, <code>lab6_slideshow</code>.</li>
<li>Поместите изображения <code>7.png</code>, <code>8.png</code>, <code>9.png</code>, <code>6.png</code> (или любые другие) в эту папку.</li>
<li>Создайте файл <code>lab6_slideshow_auto.html</code> и скопируйте в него предоставленный код.</li>
<li>Откройте файл в браузере. Нажмите кнопку “Начать”. Изображения должны автоматически меняться.</li>
</ol>
<hr>
<p><strong>Задание 1 (стр. 52) - Вариант 1 (Автомобили: подсказки и hover)</strong></p>
<p><strong>Задача:</strong> При наведении курсора мыши на фото автомобиля, в текстовом поле формы появляется сообщение о его марке и стоимости. При уведении курсора в сторону сообщение исчезает.</p>
<p><strong>Решено:</strong> Комбинация <code>onMouseOver</code>/<code>onMouseOut</code> и <code>getElementById().value</code>.</p>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>car1.jpg</code>, <code>car2.jpg</code>, <code>car3.jpg</code>, <code>car4.jpg</code> (изображения автомобилей)</li>
</ul>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab6_task1_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Автомобили<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f8ff</span><span class="token punctuation">;</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#333</span><span class="token punctuation">;</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#0056b3</span><span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.car-gallery</span> </span><span class="token punctuation">{</span> <span class="token property">display</span><span class="token punctuation">:</span> grid<span class="token punctuation">;</span> <span class="token property">grid-template-columns</span><span class="token punctuation">:</span> <span class="token function">repeat</span><span class="token punctuation">(</span><span class="token number">2</span>, <span class="token number">1</span>fr<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token property">gap</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">800</span>px<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span> auto<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.car-item</span> </span><span class="token punctuation">{</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ddd</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">8</span>px<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#fff</span><span class="token punctuation">;</span> <span class="token property">box-shadow</span><span class="token punctuation">:</span> <span class="token number">0</span> <span class="token number">2</span>px <span class="token number">4</span>px <span class="token function">rgba</span><span class="token punctuation">(</span><span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0</span>,<span class="token number">0.1</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.car-item</span> img </span><span class="token punctuation">{</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">height</span><span class="token punctuation">:</span> auto<span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span> auto<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#infoDisplay</span> </span><span class="token punctuation">{</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">600</span>px<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">border-radius</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">1.1</span>em<span class="token punctuation">;</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// данные об автомобилях: марка, цена</span>
        <span class="token keyword">var</span> carInfo <span class="token operator">=</span> <span class="token punctuation">{</span>
            <span class="token string">'car1.jpg'</span><span class="token punctuation">:</span> <span class="token string">'Ford. $40000'</span><span class="token punctuation">,</span>
            <span class="token string">'car2.jpg'</span><span class="token punctuation">:</span> <span class="token string">'Chevrolet. $35000'</span><span class="token punctuation">,</span>
            <span class="token string">'car3.jpg'</span><span class="token punctuation">:</span> <span class="token string">'Toyota. $28000'</span><span class="token punctuation">,</span>
            <span class="token string">'car4.jpg'</span><span class="token punctuation">:</span> <span class="token string">'Honda. $32000'</span>
        <span class="token punctuation">}</span><span class="token punctuation">;</span>

        <span class="token keyword">function</span> <span class="token function">showCarInfo</span><span class="token punctuation">(</span>imageName<span class="token punctuation">)</span> <span class="token punctuation">{</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'infoDisplay'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> carInfo<span class="token punctuation">[</span>imageName<span class="token punctuation">]</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>

        <span class="token keyword">function</span> <span class="token function">clearCarInfo</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'infoDisplay'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">''</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Продаются автомобили:<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>car-gallery<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>car-item<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>car1.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Ford<span class="token punctuation">"</span></span>
                 <span class="token attr-name">onMouseOver</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showCarInfo(<span class="token punctuation">'</span>car1.jpg<span class="token punctuation">'</span>);<span class="token punctuation">"</span></span>
                 <span class="token attr-name">onMouseOut</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>clearCarInfo();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>car-item<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>car2.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Chevrolet<span class="token punctuation">"</span></span>
                 <span class="token attr-name">onMouseOver</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showCarInfo(<span class="token punctuation">'</span>car2.jpg<span class="token punctuation">'</span>);<span class="token punctuation">"</span></span>
                 <span class="token attr-name">onMouseOut</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>clearCarInfo();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>car-item<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>car3.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Toyota<span class="token punctuation">"</span></span>
                 <span class="token attr-name">onMouseOver</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showCarInfo(<span class="token punctuation">'</span>car3.jpg<span class="token punctuation">'</span>);<span class="token punctuation">"</span></span>
                 <span class="token attr-name">onMouseOut</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>clearCarInfo();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>car-item<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>car4.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Honda<span class="token punctuation">"</span></span>
                 <span class="token attr-name">onMouseOver</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showCarInfo(<span class="token punctuation">'</span>car4.jpg<span class="token punctuation">'</span>);<span class="token punctuation">"</span></span>
                 <span class="token attr-name">onMouseOut</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>clearCarInfo();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>infoDisplay<span class="token punctuation">"</span></span> <span class="token attr-name">readonly</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображения:</strong> Скачайте или создайте <code>car1.jpg</code>, <code>car2.jpg</code>, <code>car3.jpg</code>, <code>car4.jpg</code> и поместите их в папку.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab6_task1_var1.html</code> в браузере. Наведите курсор на изображения автомобилей и убедитесь, что информация о них появляется в текстовом поле.</p>
</li>
</ol>
<hr>
<p><strong>Задание 2 (стр. 52) - Вариант 1 (Автомобили: слайд-шоу по кнопке)</strong></p>
<p><strong>Задача:</strong> Организовать показ слайд-шоу из тех же картинок, чтобы каждая следующая картинка показывалась не автоматически, а при нажатии кнопки.</p>
<p><strong>Решено:</strong> Модификация Примера 3 (слайд-шоу), но вместо <code>setTimeout()</code> используется кнопка для переключения.</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab6_task2_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Слайд-шоу автомобилей<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f8ff</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">img </span><span class="token punctuation">{</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">600</span>px<span class="token punctuation">;</span> <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">400</span>px<span class="token punctuation">;</span> <span class="token property">object-fit</span><span class="token punctuation">:</span> contain<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">2</span>px solid <span class="token hexcode">#555</span><span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#333</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="button"]</span> </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">12</span>px <span class="token number">25</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">18</span>px<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> currentImageIndex <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> carImages <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Array</span><span class="token punctuation">(</span><span class="token string">'car1.jpg'</span><span class="token punctuation">,</span> <span class="token string">'car2.jpg'</span><span class="token punctuation">,</span> <span class="token string">'car3.jpg'</span><span class="token punctuation">,</span> <span class="token string">'car4.jpg'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">function</span> <span class="token function">showNextImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> slideshowImg <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'slideshowCar'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Проверяем, не вышел ли индекс за пределы массива</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>currentImageIndex <span class="token operator">&gt;=</span> carImages<span class="token punctuation">.</span>length<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                currentImageIndex <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Начинаем сначала</span>
            <span class="token punctuation">}</span>
            
            slideshowImg<span class="token punctuation">.</span>src <span class="token operator">=</span> carImages<span class="token punctuation">[</span>currentImageIndex<span class="token punctuation">]</span><span class="token punctuation">;</span>
            currentImageIndex<span class="token operator">++</span><span class="token punctuation">;</span> <span class="token comment">// Подготавливаем индекс для следующего изображения</span>
        <span class="token punctuation">}</span>

        <span class="token comment">// Инициализация при загрузке, чтобы первое изображение сразу показалось</span>
        window<span class="token punctuation">.</span>onload <span class="token operator">=</span> showNextImage<span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Слайд-шоу автомобилей<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>slideshowCar<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Автомобиль<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Показать следующую<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showNextImage();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображения:</strong> Используйте те же <code>car1.jpg</code>, <code>car2.jpg</code>, <code>car3.jpg</code>, <code>car4.jpg</code> из предыдущего задания.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab6_task2_var1.html</code> в браузере. Нажимайте кнопку “Показать следующую” для переключения изображений.</p>
</li>
</ol>
<hr>
<p><strong>Задание 1 (стр. 54) - Вариант 2 (Животные: подсказки и hover)</strong></p>
<p><strong>Задача:</strong> При наведении курсора мыши на название животного в ячейке таблицы, появляется рисунок этого животного. При уведении курсора в сторону рисунок исчезает (т.е. подставляется пустой рисунок <code>empty-1.gif</code>).</p>
<p><strong>Решено:</strong> Поддержка <code>onMouseOver</code>/<code>onMouseOut</code> для ячеек таблицы (<code>&lt;td&gt;</code>), изменение <code>src</code> у <code>&lt;img&gt;</code> элемента.</p>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>gippopotam-1.gif</code></li>
<li><code>akula-1.gif</code></li>
<li><code>hobot-1.gif</code></li>
<li><code>empty-1.gif</code> (прозрачное или очень маленькое белое изображение)</li>
</ul>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab6_task1_var2.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Животные: Подсказки с изображениями<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f5f5dc</span><span class="token punctuation">;</span> <span class="token comment">/* Светлый фон */</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#333</span><span class="token punctuation">;</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#8b4513</span><span class="token punctuation">;</span> <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">table </span><span class="token punctuation">{</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span> <span class="token property">border-collapse</span><span class="token punctuation">:</span> collapse<span class="token punctuation">;</span> <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">300</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">td </span><span class="token punctuation">{</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">td<span class="token pseudo-class">:hover</span> </span><span class="token punctuation">{</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#ffe4b5</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#animal-image</span> </span><span class="token punctuation">{</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">200</span>px<span class="token punctuation">;</span> <span class="token property">height</span><span class="token punctuation">:</span> auto<span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ddd</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Карта соответствия названий животных и файлов изображений</span>
        <span class="token keyword">var</span> animalImages <span class="token operator">=</span> <span class="token punctuation">{</span>
            <span class="token string">'БЕГЕМОТ'</span><span class="token punctuation">:</span> <span class="token string">'gippopotam-1.gif'</span><span class="token punctuation">,</span>
            <span class="token string">'АКУЛА'</span><span class="token punctuation">:</span> <span class="token string">'akula-1.gif'</span><span class="token punctuation">,</span>
            <span class="token string">'МАМОНТ'</span><span class="token punctuation">:</span> <span class="token string">'hobot-1.gif'</span>
        <span class="token punctuation">}</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> emptyImage <span class="token operator">=</span> <span class="token string">'empty-1.gif'</span><span class="token punctuation">;</span> <span class="token comment">// Пустое изображение</span>

        <span class="token keyword">function</span> <span class="token function">showAnimalImage</span><span class="token punctuation">(</span>animalName<span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> imgElement <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'animal-image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>animalImages<span class="token punctuation">[</span>animalName<span class="token punctuation">]</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                imgElement<span class="token punctuation">.</span>src <span class="token operator">=</span> animalImages<span class="token punctuation">[</span>animalName<span class="token punctuation">]</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>

        <span class="token keyword">function</span> <span class="token function">hideAnimalImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'animal-image'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>src <span class="token operator">=</span> emptyImage<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>

        <span class="token comment">// Инициализация изображения при загрузке</span>
        window<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> imgElement <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'animal-image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            imgElement<span class="token punctuation">.</span>src <span class="token operator">=</span> emptyImage<span class="token punctuation">;</span> <span class="token comment">// Помним про empty-1.gif</span>
        <span class="token punctuation">}</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Наведи курсор на название животного<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>table</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span> <span class="token attr-name">onMouseOver</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showAnimalImage(<span class="token punctuation">'</span>БЕГЕМОТ<span class="token punctuation">'</span>);<span class="token punctuation">"</span></span> <span class="token attr-name">onMouseOut</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>hideAnimalImage();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>БЕГЕМОТ<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span> <span class="token attr-name">onMouseOver</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showAnimalImage(<span class="token punctuation">'</span>АКУЛА<span class="token punctuation">'</span>);<span class="token punctuation">"</span></span> <span class="token attr-name">onMouseOut</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>hideAnimalImage();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>АКУЛА<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span> <span class="token attr-name">onMouseOver</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showAnimalImage(<span class="token punctuation">'</span>МАМОНТ<span class="token punctuation">'</span>);<span class="token punctuation">"</span></span> <span class="token attr-name">onMouseOut</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>hideAnimalImage();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>МАМОНТ<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>table</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>animal-image<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Изображение животного<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображения:</strong> Скачайте или создайте <code>gippopotam-1.gif</code>, <code>akula-1.gif</code>, <code>hobot-1.gif</code>, а также <code>empty-1.gif</code> (можно взять 1x1 пиксель белого или прозрачного цвета). Поместите их в папку.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab6_task1_var2.html</code> в браузере. Наведите курсор на названия животных, и убедитесь, что изображения появляются/исчезают.</p>
</li>
</ol>
<hr>
<p><strong>Задание 2 (стр. 54) - Вариант 2 (Животные: слайд-шоу по кнопке)</strong></p>
<p><strong>Задача:</strong> Организовать показ слайд-шоу из тех же картинок животных, чтобы каждая следующая картинка показывалась не автоматически, а при нажатии кнопки.</p>
<p><strong>Решено:</strong> Модификация слайд-шоу, аналогичная Заданию 2 Варианта 1 (Автомобили), но с изображениями животных.</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab6_task2_var2.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Слайд-шоу животных<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f5f5dc</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">img </span><span class="token punctuation">{</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">600</span>px<span class="token punctuation">;</span> <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">400</span>px<span class="token punctuation">;</span> <span class="token property">object-fit</span><span class="token punctuation">:</span> contain<span class="token punctuation">;</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">2</span>px solid <span class="token hexcode">#555</span><span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#333</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="button"]</span> </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">12</span>px <span class="token number">25</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">18</span>px<span class="token punctuation">;</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> currentAnimalIndex <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
        <span class="token comment">// Массив изображений животных</span>
        <span class="token keyword">var</span> animalSlides <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Array</span><span class="token punctuation">(</span><span class="token string">'gippopotam-1.gif'</span><span class="token punctuation">,</span> <span class="token string">'akula-1.gif'</span><span class="token punctuation">,</span> <span class="token string">'hobot-1.gif'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">function</span> <span class="token function">showNextAnimal</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> slideshowAnimalImg <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'slideshowAnimal'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Проверяем, не вышел ли индекс за пределы массива</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>currentAnimalIndex <span class="token operator">&gt;=</span> animalSlides<span class="token punctuation">.</span>length<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                currentAnimalIndex <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Начинаем сначала</span>
            <span class="token punctuation">}</span>
            
            slideshowAnimalImg<span class="token punctuation">.</span>src <span class="token operator">=</span> animalSlides<span class="token punctuation">[</span>currentAnimalIndex<span class="token punctuation">]</span><span class="token punctuation">;</span>
            currentAnimalIndex<span class="token operator">++</span><span class="token punctuation">;</span> <span class="token comment">// Подготавливаем индекс для следующего изображения</span>
        <span class="token punctuation">}</span>

        <span class="token comment">// Инициализация при загрузке, чтобы первое изображение сразу показалось</span>
        window<span class="token punctuation">.</span>onload <span class="token operator">=</span> showNextAnimal<span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Слайд-шоу животных<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>slideshowAnimal<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Животное<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Показать следующую<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>showNextAnimal();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображения:</strong> Используйте те же <code>gippopotam-1.gif</code>, <code>akula-1.gif</code>, <code>hobot-1.gif</code> из предыдущего задания.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab6_task2_var2.html</code> в браузере. Нажимайте кнопку “Показать следующую” для переключения изображений.</p>
</li>
</ol>
<hr>
<p>Это завершает <strong>ЛАБОРАТОРНУЮ РАБОТУ № 6</strong>.</p>
<p>Отлично! Переходим к <strong>ЛАБОРАТОРНОЙ РАБОТЕ № 7: Свойство <code>style</code>. Объект <code>style</code> и его свойства</strong>.</p>
<hr>
<h3 id="лабораторная-работа-№-7-свойство-style.-объект-style-и-его-свойства"><strong>ЛАБОРАТОРНАЯ РАБОТА № 7: Свойство <code>style</code>. Объект <code>style</code> и его свойства</strong></h3>
<p><strong>Цель:</strong> Изучить динамическое изменение CSS-стилей HTML-элементов с использованием JavaScript. Основное внимание будет уделено свойству <code>style</code> каждого HTML-элемента, которое само является объектом <code>CSSStyleDeclaration</code> и содержит все inline-стили элемента.</p>
<p><strong>Общее описание:</strong></p>
<ul>
<li><strong><code>element.style</code>:</strong> Это свойство любого HTML-элемента, к которому мы можем получить доступ в JavaScript (например, через <code>document.getElementById()</code>). Оно представляет собой объект, содержащий CSS-свойства.</li>
<li><strong>Доступ к CSS-свойствам:</strong> К свойствам CSS через <code>element.style</code> обращаются с использованием camelCase нотации (например, <code>background-color</code> становится <code>backgroundColor</code>, <code>font-size</code> становится <code>fontSize</code>).</li>
<li><strong>Значения стилей:</strong> Значения присваиваются как строки (например, <code>element.style.color = 'red';</code>).</li>
<li><strong>Свойство <code>display</code>:</strong> Позволяет управлять отображением элемента (<code>block</code>, <code>none</code>, <code>inline</code>). <code>display: none</code> скрывает элемент и не оставляет для него места в DOM.</li>
<li><strong>Позиционирование элементов:</strong> Изменение свойств <code>top</code> и <code>left</code> (<code>position: absolute</code> или <code>relative</code> обязательно) для перемещения элементов.</li>
</ul>
<hr>
<p><strong>Примеры из пособия (стр. 55-59) и их выполнение:</strong></p>
<p><strong>Пример 1 (стр. 55) - Изменение цвета буквы и текста кнопки</strong></p>
<p>Демонстрирует изменение цвета текста элемента (<code>h1</code>) и значения текста кнопки при каждом клике.</p>
<p><strong>Код для Примера 1:</strong></p>
<p><strong>Файл: <code>lab7_toggle_color.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Изменение цвета буквы и кнопки<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">h1 </span><span class="token punctuation">{</span>
            <span class="token property">color</span><span class="token punctuation">:</span> red<span class="token punctuation">;</span> <span class="token comment">/* Изначальный цвет буквы */</span>
            <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">36</span>pt<span class="token punctuation">;</span>
            <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f8ff</span><span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">flex-direction</span><span class="token punctuation">:</span> column<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">justify-content</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">min-height</span><span class="token punctuation">:</span> <span class="token number">80</span>vh<span class="token punctuation">;</span><span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="button"]</span> </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span><span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> isRed <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span> <span class="token comment">// Флаг: true, если буква красная; false, если зеленая</span>

        <span class="token keyword">function</span> <span class="token function">toggleColorAndButton</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Получаем ссылки на элемент h1 (буква Z) и кнопку</span>
            <span class="token keyword">var</span> letterElement <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'letterZ'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> buttonElement <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'toggleButton'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>isRed<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token comment">// Если сейчас красный, меняем на зеленый</span>
                letterElement<span class="token punctuation">.</span>style<span class="token punctuation">.</span>color <span class="token operator">=</span> <span class="token string">'green'</span><span class="token punctuation">;</span>
                buttonElement<span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">'Изменить на красный'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token comment">// Если сейчас зеленый, меняем на красный</span>
                letterElement<span class="token punctuation">.</span>style<span class="token punctuation">.</span>color <span class="token operator">=</span> <span class="token string">'red'</span><span class="token punctuation">;</span>
                buttonElement<span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">'Изменить на зеленый'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            isRed <span class="token operator">=</span> <span class="token operator">!</span>isRed<span class="token punctuation">;</span> <span class="token comment">// Переключаем флаг</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>letterZ<span class="token punctuation">'</span></span><span class="token punctuation">&gt;</span></span>Z<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>toggleButton<span class="token punctuation">'</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Изменить на зеленый<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggleColorAndButton();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Сохраните файл как <code>lab7_toggle_color.html</code>.</li>
<li>Откройте файл в браузере. Нажимайте кнопку и наблюдайте за изменением цвета буквы “Z” и текста на кнопке.</li>
</ol>
<hr>
<p><strong>Пример 2 (стр. 57) - Появление/исчезновение картинки (<code>display</code> свойство)</strong></p>
<p>Демонстрирует, как показывать и скрывать элемент (изображение) с использованием свойства CSS <code>display</code> (<code>block</code> и <code>none</code>).</p>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>bird2.gif</code> (любое изображение, можно использовать из предыдущих лабораторных)</li>
</ul>
<p><strong>Код для Примера 2:</strong></p>
<p><strong>Файл: <code>lab7_toggle_display.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Появление/исчезновение картинки<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f8ff</span><span class="token punctuation">;</span> <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span> <span class="token property">flex-direction</span><span class="token punctuation">:</span> column<span class="token punctuation">;</span> <span class="token property">align-items</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">justify-content</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">min-height</span><span class="token punctuation">:</span> <span class="token number">80</span>vh<span class="token punctuation">;</span><span class="token punctuation">}</span>
        <span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#333</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">img </span><span class="token punctuation">{</span> <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#ccc</span><span class="token punctuation">;</span> <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">300</span>px<span class="token punctuation">;</span> <span class="token property">height</span><span class="token punctuation">:</span> auto<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">input<span class="token attribute">[type="button"]</span> </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">toggleDisplay</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Получаем ссылку на изображение по id 'myImage'</span>
            <span class="token keyword">var</span> imgElement <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'myImage'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Проверяем текущее значение свойства 'display'</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>imgElement<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">===</span> <span class="token string">'none'</span> <span class="token operator">||</span> imgElement<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">===</span> <span class="token string">''</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token comment">// Если скрыто или не задано, делаем видимым (block)</span>
                imgElement<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'block'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token comment">// Если видимо, делаем скрытым (none)</span>
                imgElement<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'none'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>
        
        <span class="token comment">// Изначально скрываем картинку при загрузке страницы, если она не скрыта в CSS</span>
        window<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> imgElement <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'myImage'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>imgElement<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                imgElement<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'none'</span><span class="token punctuation">;</span> <span class="token comment">// Чтобы изначально была скрыта</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Покажи/Спрячь картинку<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>myImage<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bird2.gif<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Птичка<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>button<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Нажми меня<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggleDisplay();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Поместите изображение <code>bird2.gif</code> (или любое другое) в ту же папку.</li>
<li>Сохраните файл как <code>lab7_toggle_display.html</code>.</li>
<li>Откройте файл в браузере. Нажимайте кнопку и наблюдайте за появлением/исчезновением картинки.</li>
</ol>
<hr>
<p><strong>Пример 3 (стр. 58) - Движение объекта по горизонтали (<code>setTimeout</code>)</strong></p>
<p>Демонстрирует анимацию движения объекта (изображения) по горизонтали с использованием <code>position: absolute</code>, <code>left</code> и <code>setTimeout()</code>.</p>
<p><strong>Необходимые файлы:</strong></p>
<ul>
<li><code>p5_0.jpg</code> (фоновое изображение)</li>
<li><code>bird2.gif</code> (движущееся изображение)</li>
</ul>
<p><strong>Код для Примера 3:</strong></p>
<p><strong>Файл: <code>lab7_move_horizontal.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Движение картинки по горизонтали<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token property">overflow</span><span class="token punctuation">:</span> hidden<span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#background-image</span> </span><span class="token punctuation">{</span>
            <span class="token property">position</span><span class="token punctuation">:</span> absolute<span class="token punctuation">;</span>
            <span class="token property">top</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
            <span class="token property">left</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
            <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token comment">/* Фон на всю ширину окна */</span>
            <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> <span class="token comment">/* Фон на всю высоту окна */</span>
            <span class="token property">object-fit</span><span class="token punctuation">:</span> cover<span class="token punctuation">;</span> <span class="token comment">/* Чтобы фон заполнял и не искажался */</span>
            <span class="token property">z-index</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">/* Нижний слой */</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#moving-image</span> </span><span class="token punctuation">{</span>
            <span class="token property">position</span><span class="token punctuation">:</span> absolute<span class="token punctuation">;</span>
            <span class="token property">top</span><span class="token punctuation">:</span> <span class="token number">100</span>px<span class="token punctuation">;</span> <span class="token comment">/* Фиксированная высота */</span>
            <span class="token property">left</span><span class="token punctuation">:</span> <span class="token number">0</span>px<span class="token punctuation">;</span> <span class="token comment">/* Начальная позиция X */</span>
            <span class="token property">z-index</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">;</span> <span class="token comment">/* Верхний слой */</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> movingImage<span class="token punctuation">;</span> <span class="token comment">// Ссылка на двигающееся изображение</span>
        <span class="token keyword">var</span> backgroundImage<span class="token punctuation">;</span> <span class="token comment">// Ссылка на фоновое изображение</span>
        <span class="token keyword">var</span> currentX <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Текущая позиция по X</span>
        <span class="token keyword">var</span> step <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span> <span class="token comment">// Шаг движения в пикселях</span>

        window<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            movingImage <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'moving-image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            backgroundImage <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'background-image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Убедимся, что изображения загрузились и их размеры доступны</span>
            <span class="token comment">// Используем 'load' событие для движущейся картинки</span>
            movingImage<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token comment">// Только после загрузки изображений начинаем движение</span>
                <span class="token function">startAnimation</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
            <span class="token punctuation">}</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>movingImage<span class="token punctuation">.</span>complete<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Если изображение уже загружено из кэша</span>
                <span class="token function">startAnimation</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span><span class="token punctuation">;</span>

        <span class="token keyword">function</span> <span class="token function">startAnimation</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token function">moveImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Запускаем анимацию</span>
        <span class="token punctuation">}</span>

        <span class="token keyword">function</span> <span class="token function">moveImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> bgWidth <span class="token operator">=</span> backgroundImage<span class="token punctuation">.</span>offsetWidth<span class="token punctuation">;</span> <span class="token comment">// Ширина фона</span>
            <span class="token keyword">var</span> imgWidth <span class="token operator">=</span> movingImage<span class="token punctuation">.</span>offsetWidth<span class="token punctuation">;</span> <span class="token comment">// Ширина движущегося изображения</span>

            currentX <span class="token operator">+=</span> step<span class="token punctuation">;</span> <span class="token comment">// Увеличиваем позицию X</span>

            <span class="token comment">// Если достигли правой границы фона</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>currentX <span class="token operator">+</span> imgWidth <span class="token operator">&gt;=</span> bgWidth<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                currentX <span class="token operator">=</span> bgWidth <span class="token operator">-</span> imgWidth<span class="token punctuation">;</span> <span class="token comment">// Устанавливаем точно у края</span>
                <span class="token comment">// Можно остановить или начать с начала</span>
                <span class="token comment">// currentX = 0; // Для повторения движения по кругу</span>
                console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Достигли края, остановка."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span> <span class="token comment">// Останавливаем анимацию</span>
            <span class="token punctuation">}</span>

            movingImage<span class="token punctuation">.</span>style<span class="token punctuation">.</span>left <span class="token operator">=</span> currentX <span class="token operator">+</span> <span class="token string">'px'</span><span class="token punctuation">;</span> <span class="token comment">// Обновляем позицию</span>

            <span class="token comment">// Вызываем эту же функцию через 50 мс</span>
            <span class="token function">setTimeout</span><span class="token punctuation">(</span>moveImage<span class="token punctuation">,</span> <span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>background-image<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>p5_0.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Фон<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>moving-image<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bird2.gif<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Движущаяся картинка<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Поместите изображения <code>p5_0.jpg</code> и <code>bird2.gif</code> в ту же папку.</li>
<li>Сохраните файл как <code>lab7_move_horizontal.html</code>.</li>
<li>Откройте файл в браузере. Вы должны увидеть, как <code>bird2.gif</code> движется по горизонтали.</li>
</ol>
<hr>
<p><strong>Пример 4 (стр. 59) - Движение объекта по диагонали (<code>setTimeout</code>)</strong></p>
<p>Изменяет предыдущий пример так, чтобы рисунок двигался по “главной диагонали” (вниз-вправо), затем менял направление (вверх-влево), и так далее.</p>
<p><strong>Код для Примера 4:</strong></p>
<p><strong>Файл: <code>lab7_move_diagonal.html</code></strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Движение картинки по диагонали<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token property">overflow</span><span class="token punctuation">:</span> hidden<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f8ff</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#background-image</span> </span><span class="token punctuation">{</span>
            <span class="token property">position</span><span class="token punctuation">:</span> absolute<span class="token punctuation">;</span>
            <span class="token property">top</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
            <span class="token property">left</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
            <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span>
            <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span>
            <span class="token property">object-fit</span><span class="token punctuation">:</span> cover<span class="token punctuation">;</span>
            <span class="token property">z-index</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#moving-image</span> </span><span class="token punctuation">{</span>
            <span class="token property">position</span><span class="token punctuation">:</span> absolute<span class="token punctuation">;</span>
            <span class="token property">top</span><span class="token punctuation">:</span> <span class="token number">0</span>px<span class="token punctuation">;</span>
            <span class="token property">left</span><span class="token punctuation">:</span> <span class="token number">0</span>px<span class="token punctuation">;</span>
            <span class="token property">z-index</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> movingImage<span class="token punctuation">;</span>
        <span class="token keyword">var</span> backgroundImage<span class="token punctuation">;</span>
        <span class="token keyword">var</span> currentX <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> currentY <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> step <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">;</span> <span class="token comment">// Шаг движения по X и Y</span>
        <span class="token keyword">var</span> directionX <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// 1: вправо, -1: влево</span>
        <span class="token keyword">var</span> directionY <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// 1: вниз, -1: вверх</span>

        window<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            movingImage <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'moving-image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            backgroundImage <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'background-image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Убеждаемся, что изображения загрузились</span>
            movingImage<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">moveImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>movingImage<span class="token punctuation">.</span>complete<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">moveImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span><span class="token punctuation">;</span>

        <span class="token keyword">function</span> <span class="token function">moveImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> bgWidth <span class="token operator">=</span> backgroundImage<span class="token punctuation">.</span>offsetWidth<span class="token punctuation">;</span>
            <span class="token keyword">var</span> bgHeight <span class="token operator">=</span> backgroundImage<span class="token punctuation">.</span>offsetHeight<span class="token punctuation">;</span>
            <span class="token keyword">var</span> imgWidth <span class="token operator">=</span> movingImage<span class="token punctuation">.</span>offsetWidth<span class="token punctuation">;</span>
            <span class="token keyword">var</span> imgHeight <span class="token operator">=</span> movingImage<span class="token punctuation">.</span>offsetHeight<span class="token punctuation">;</span>

            currentX <span class="token operator">+=</span> step <span class="token operator">*</span> directionX<span class="token punctuation">;</span>
            currentY <span class="token operator">+=</span> step <span class="token operator">*</span> directionY<span class="token punctuation">;</span>

            <span class="token comment">// Проверка и смена направления по X</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>currentX <span class="token operator">+</span> imgWidth <span class="token operator">&gt;=</span> bgWidth<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                currentX <span class="token operator">=</span> bgWidth <span class="token operator">-</span> imgWidth<span class="token punctuation">;</span> <span class="token comment">// Устанавливаем точно у края</span>
                directionX <span class="token operator">=</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Меняем на движение влево</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>currentX <span class="token operator">&lt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                currentX <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Устанавливаем точно у края</span>
                directionX <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Меняем на движение вправо</span>
            <span class="token punctuation">}</span>

            <span class="token comment">// Проверка и смена направления по Y</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>currentY <span class="token operator">+</span> imgHeight <span class="token operator">&gt;=</span> bgHeight<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                currentY <span class="token operator">=</span> bgHeight <span class="token operator">-</span> imgHeight<span class="token punctuation">;</span> <span class="token comment">// Устанавливаем точно у края</span>
                directionY <span class="token operator">=</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Меняем на движение вверх</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>currentY <span class="token operator">&lt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                currentY <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Устанавливаем точно у края</span>
                directionY <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Меняем на движение вниз</span>
            <span class="token punctuation">}</span>

            movingImage<span class="token punctuation">.</span>style<span class="token punctuation">.</span>left <span class="token operator">=</span> currentX <span class="token operator">+</span> <span class="token string">'px'</span><span class="token punctuation">;</span>
            movingImage<span class="token punctuation">.</span>style<span class="token punctuation">.</span>top <span class="token operator">=</span> currentY <span class="token operator">+</span> <span class="token string">'px'</span><span class="token punctuation">;</span>

            <span class="token function">setTimeout</span><span class="token punctuation">(</span>moveImage<span class="token punctuation">,</span> <span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Вызываем функцию снова через небольшой интервал</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>background-image<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>p5_0.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Фон<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>moving-image<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>4.gif<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Движущаяся картинка<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Инструкции по выполнению:</strong></p>
<ol>
<li>Откройте текстовый редактор.</li>
<li>Скопируйте приведенный выше код.</li>
<li>Поместите изображения <code>p5_0.jpg</code> и <code>4.gif</code> в ту же папку.</li>
<li>Сохраните файл как <code>lab7_move_diagonal.html</code>.</li>
<li>Откройте файл в браузере. Вы должны увидеть, как <code>4.gif</code> движется по диагонали, отскакивая от краев.</li>
</ol>
<hr>
<p><strong>Задание 1 (стр. 60) - Вариант 1: Изменение рамки изображения (toggle)</strong></p>
<p><strong>Задача:</strong> Создать документ, в котором рисунок <code>neznakomka3.jpg</code> заключен в рамку серого цвета типа <code>inset</code> и толщиной 50. По нажатию кнопки менять цвет рамки на синий и надпись на кнопке. При следующем нажатии изменять цвет рамки на серый и надпись на кнопке.</p>
<p><strong>Решено:</strong> (Это задание уже было выполнено в ЛР4, Задание 3, Вариант 1. Я предоставлю тот же код для целостности ЛР7, поскольку оно идеально подходит для демонстрации <code>element.style.borderColor</code>.)</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab7_task1_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Изменение рамки изображения<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">50</span>px<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f0f0</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector">img </span><span class="token punctuation">{</span>
            <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">50</span>px inset grey<span class="token punctuation">;</span> <span class="token comment">/* Изначальный стиль рамки */</span>
            <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector">button </span><span class="token punctuation">{</span> <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span> <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span> <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span> <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> isBlue <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span> <span class="token comment">// Флаг для отслеживания текущего цвета рамки</span>

        <span class="token keyword">function</span> <span class="token function">toggleBorder</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> img <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'myImage'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> button <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'toggleButton'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>isBlue<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token comment">// Сейчас синий, меняем на серый</span>
                img<span class="token punctuation">.</span>style<span class="token punctuation">.</span>borderColor <span class="token operator">=</span> <span class="token string">'grey'</span><span class="token punctuation">;</span>
                button<span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">'Изменить рамку на синий'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token comment">// Сейчас серый, меняем на синий</span>
                img<span class="token punctuation">.</span>style<span class="token punctuation">.</span>borderColor <span class="token operator">=</span> <span class="token string">'blue'</span><span class="token punctuation">;</span>
                button<span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">'Изменить рамку на серый'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            isBlue <span class="token operator">=</span> <span class="token operator">!</span>isBlue<span class="token punctuation">;</span> <span class="token comment">// Переключаем флаг</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Изменение рамки изображения<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>myImage<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>neznakomka3.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Картина<span class="token punctuation">"</span></span> <span class="token attr-name">width</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>300<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggleButton<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggleBorder();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Изменить рамку на синий<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображение <code>neznakomka3.jpg</code></strong> (или любое другое) в ту же папку.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab7_task1_var1.html</code> в браузере. Нажимайте кнопку и наблюдайте за изменением цвета рамки и текста кнопки.</p>
</li>
</ol>
<hr>
<p><strong>Задание 2 (стр. 60) - Вариант 1: Показать/Скрыть свечу (CSS <code>display</code>)</strong></p>
<p><strong>Задача:</strong> Сначала на странице только текст стихотворения и кнопка с надписью «показать свечу». При нажатии на кнопку текст стихотворения прячется, на его месте появляется рисунок, и надпись на кнопке меняется на «показать текст». Если еще раз нажать на кнопку, рисунок исчезает и появляется текст.</p>
<p><strong>Решено:</strong> (Это задание также было выполнено в ЛР4, Задание 2, Вариант 1. Оно отлично иллюстрирует <code>element.style.display</code>.)</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab7_task2_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Свеча и Стихотворение<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> 
            <span class="token property">background-color</span><span class="token punctuation">:</span> darkblue<span class="token punctuation">;</span> <span class="token comment">/* Темно-синий фон */</span>
            <span class="token property">font-family</span><span class="token punctuation">:</span> Arial, sans-serif<span class="token punctuation">;</span> 
            <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">22</span>px<span class="token punctuation">;</span> <span class="token comment">/* Размер шрифта */</span>
            <span class="token property">font-style</span><span class="token punctuation">:</span> italic<span class="token punctuation">;</span> <span class="token comment">/* Курсив */</span>
            <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span> <span class="token comment">/* Цвет шрифта белый */</span>
            <span class="token property">text-align</span><span class="token punctuation">:</span> center<span class="token punctuation">;</span>
            <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token class">.content-container</span> </span><span class="token punctuation">{</span>
            <span class="token property">max-width</span><span class="token punctuation">:</span> <span class="token number">600</span>px<span class="token punctuation">;</span>
            <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span>
            <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span>
            <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">5</span>px outset <span class="token hexcode">#ffA089</span><span class="token punctuation">;</span> <span class="token comment">/* Рамка вокруг текста/картинки */</span>
            <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#image-content</span> img </span><span class="token punctuation">{</span>
            <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">200</span>px<span class="token punctuation">;</span> <span class="token comment">/* Размер картинки */</span>
            <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">200</span>px<span class="token punctuation">;</span> <span class="token comment">/* Размер картинки */</span>
            <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">50</span>px outset <span class="token hexcode">#ffA089</span><span class="token punctuation">;</span> <span class="token comment">/* Рамка вокруг картинки, толщина 50 */</span>
            <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span> <span class="token comment">/* Отступы по 5 */</span>
            <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector">button </span><span class="token punctuation">{</span>
            <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">20</span>px<span class="token punctuation">;</span>
            <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">18</span>px<span class="token punctuation">;</span>
            <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span>
            <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> showingText <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span> <span class="token comment">// Флаг: true - показывается текст, false - показывается картинка</span>

        <span class="token keyword">function</span> <span class="token function">toggleContent</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> textDiv <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'text-content'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> imageDiv <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'image-content'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> toggleButton <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'toggle-button'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>showingText<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token comment">// Скрываем текст, показываем картинку</span>
                textDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'none'</span><span class="token punctuation">;</span>
                imageDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'block'</span><span class="token punctuation">;</span>
                toggleButton<span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">'Показать текст'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token comment">// Скрываем картинку, показываем текст</span>
                imageDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'none'</span><span class="token punctuation">;</span> 
                textDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'block'</span><span class="token punctuation">;</span> 
                toggleButton<span class="token punctuation">.</span>value <span class="token operator">=</span> <span class="token string">'Показать свечу'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            showingText <span class="token operator">=</span> <span class="token operator">!</span>showingText<span class="token punctuation">;</span> <span class="token comment">// Переключаем флаг</span>
        <span class="token punctuation">}</span>

        <span class="token comment">// Инициализация: убедимся, что изображение скрыто при загрузке</span>
        window<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'image-content'</span><span class="token punctuation">)</span><span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'none'</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>content-container<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text-content<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h3</span><span class="token punctuation">&gt;</span></span>Иннокентий Анненский<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h3</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h2</span><span class="token punctuation">&gt;</span></span>Свечку внесли<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h2</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Не мерещится ль вам иногда,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Когда сумерки ходят по дому,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Тут же возле иная среда,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Где живем мы совсем по-другому?<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>С тенью тень там так мягко слилась,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Там бывает такая минута,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Что лучами незримыми глаз<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Мы уходим друг в друга как будто.<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>И движеньем спугнуть этот миг<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Мы боимся, иль словом нарушить,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Точно ухом кто возле приник,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Заставляя далекое слушать.<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Но едва запылает свеча,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Чуткий мир уступает без боя,<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Лишь из глаз по наклонам луча<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Тени в пламя сбегут голубое.<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>image-content<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>свеча1.gif<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Свеча<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggle-button<span class="token punctuation">"</span></span> <span class="token attr-name">onClick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggleContent();<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Показать свечу<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображение <code>свеча1.gif</code></strong> в ту же папку.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab7_task2_var1.html</code> в браузере. Нажимайте кнопку для переключения между текстом и изображением.</p>
</li>
</ol>
<hr>
<p><strong>Задание 3 (стр. 60) - Вариант 1: Движение картинки по сложной траектории</strong></p>
<p><strong>Задача:</strong> Создать документ, в котором рисунок <code>p5_0.jpg</code> занимает 50% окна и является нижним слоем. На верхнем слое второй рисунок <code>4.gif</code>, который двигается по горизонтали к правой границе первого рисунка, затем на строку (высоту рисунка) вниз и назад, к левой границе, на строку вниз и к правой границе, и т.д. до нижней границы первого рисунка.</p>
<p><strong>Решено:</strong> (Это задание уже было выполнено в ЛР4, Задание 3, Вариант 1. Я предоставлю тот же код.)</p>
<p><strong>Пошаговая инструкция для выполнения:</strong></p>
<ol>
<li>
<p><strong>Создайте HTML-файл:</strong> Сохраните пустой файл как <code>lab7_task3_var1.html</code>.</p>
</li>
<li>
<p><strong>Базовая HTML-структура <code>lab7_task3_var1.html</code>:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Движение картинки по сложной траектории<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token property">overflow</span><span class="token punctuation">:</span> hidden<span class="token punctuation">;</span> <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#f0f8ff</span><span class="token punctuation">;</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#background-image</span> </span><span class="token punctuation">{</span>
            <span class="token property">position</span><span class="token punctuation">:</span> absolute<span class="token punctuation">;</span>
            <span class="token property">top</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
            <span class="token property">left</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
            <span class="token comment">/* Задание говорит "50% окна", но здесь stretch to fill */</span>
            <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span> 
            <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">100%</span><span class="token punctuation">;</span>
            <span class="token property">object-fit</span><span class="token punctuation">:</span> cover<span class="token punctuation">;</span>
            <span class="token property">z-index</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#moving-image</span> </span><span class="token punctuation">{</span>
            <span class="token property">position</span><span class="token punctuation">:</span> absolute<span class="token punctuation">;</span>
            <span class="token property">top</span><span class="token punctuation">:</span> <span class="token number">0</span>px<span class="token punctuation">;</span>
            <span class="token property">left</span><span class="token punctuation">:</span> <span class="token number">0</span>px<span class="token punctuation">;</span>
            <span class="token property">z-index</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> movingImage<span class="token punctuation">;</span>
        <span class="token keyword">var</span> backgroundImage<span class="token punctuation">;</span>
        <span class="token keyword">var</span> currentX <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> currentY <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> step <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">;</span> <span class="token comment">// Шаг движения</span>
        <span class="token keyword">var</span> directionX <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// 1: вправо, -1: влево</span>
        <span class="token keyword">var</span> directionY <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// 0: не двигаемся по Y, 1: двигаемся вниз, -1: двигаемся вверх</span>

        <span class="token comment">// Для отслеживания состояний: 0 = вправо, 1 = вниз+влево, 2 = вниз+вправо</span>
        <span class="token keyword">var</span> movementState <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> 
        <span class="token keyword">var</span> lineChangeY <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Сколько раз мы сместились по Y</span>

        window<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            movingImage <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'moving-image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            backgroundImage <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'background-image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            
            <span class="token comment">// Чтобы размеры были актуальны</span>
            movingImage<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">moveImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span><span class="token punctuation">;</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>movingImage<span class="token punctuation">.</span>complete<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">moveImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span><span class="token punctuation">;</span>

        <span class="token keyword">function</span> <span class="token function">moveImage</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> bgWidth <span class="token operator">=</span> backgroundImage<span class="token punctuation">.</span>offsetWidth<span class="token punctuation">;</span>
            <span class="token keyword">var</span> bgHeight <span class="token operator">=</span> backgroundImage<span class="token punctuation">.</span>offsetHeight<span class="token punctuation">;</span>
            <span class="token keyword">var</span> imgWidth <span class="token operator">=</span> movingImage<span class="token punctuation">.</span>offsetWidth<span class="token punctuation">;</span>
            <span class="token keyword">var</span> imgHeight <span class="token operator">=</span> movingImage<span class="token punctuation">.</span>offsetHeight<span class="token punctuation">;</span>

            <span class="token keyword">var</span> nextX <span class="token operator">=</span> currentX <span class="token operator">+</span> step <span class="token operator">*</span> directionX<span class="token punctuation">;</span>
            <span class="token keyword">var</span> nextY <span class="token operator">=</span> currentY<span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>movementState <span class="token operator">===</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Движение вправо до края</span>
                <span class="token keyword">if</span> <span class="token punctuation">(</span>nextX <span class="token operator">+</span> imgWidth <span class="token operator">&gt;=</span> bgWidth<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    currentX <span class="token operator">=</span> bgWidth <span class="token operator">-</span> imgWidth<span class="token punctuation">;</span>
                    movementState <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Переходим в состояние движения вниз+влево</span>
                    currentY <span class="token operator">+=</span> imgHeight<span class="token punctuation">;</span> <span class="token comment">// Сдвиг вниз</span>
                    <span class="token keyword">if</span> <span class="token punctuation">(</span>currentY <span class="token operator">+</span> imgHeight <span class="token operator">&gt;=</span> bgHeight<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Достигли низа</span>
                        console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Достигли нижней границы. Остановка."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                        <span class="token keyword">return</span><span class="token punctuation">;</span>
                    <span class="token punctuation">}</span>
                    directionX <span class="token operator">=</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Теперь влево</span>
                <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                    currentX <span class="token operator">=</span> nextX<span class="token punctuation">;</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>movementState <span class="token operator">===</span> <span class="token number">1</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Движение влево до края</span>
                 <span class="token keyword">if</span> <span class="token punctuation">(</span>nextX <span class="token operator">&lt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    currentX <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
                    movementState <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Переключаемся на движение вправо</span>
                    currentY <span class="token operator">+=</span> imgHeight<span class="token punctuation">;</span> <span class="token comment">// Сдвиг вниз</span>
                    <span class="token keyword">if</span> <span class="token punctuation">(</span>currentY <span class="token operator">+</span> imgHeight <span class="token operator">&gt;=</span> bgHeight<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Достигли низа</span>
                        console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Достигли нижней границы. Остановка."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                        <span class="token keyword">return</span><span class="token punctuation">;</span>
                    <span class="token punctuation">}</span>
                    directionX <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Теперь вправо</span>
                <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                    currentX <span class="token operator">=</span> nextX<span class="token punctuation">;</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">}</span>


            movingImage<span class="token punctuation">.</span>style<span class="token punctuation">.</span>left <span class="token operator">=</span> currentX <span class="token operator">+</span> <span class="token string">'px'</span><span class="token punctuation">;</span>
            movingImage<span class="token punctuation">.</span>style<span class="token punctuation">.</span>top <span class="token operator">=</span> currentY <span class="token operator">+</span> <span class="token string">'px'</span><span class="token punctuation">;</span>

            <span class="token function">setTimeout</span><span class="token punctuation">(</span>moveImage<span class="token punctuation">,</span> <span class="token number">50</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Вызываем функцию снова через 50 мс</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>background-image<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>p5_0.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Фон<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>moving-image<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>4.gif<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Движущаяся картинка<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
</li>
<li>
<p><strong>Поместите изображения <code>p5_0.jpg</code> и <code>4.gif</code></strong> в ту же папку.</p>
</li>
<li>
<p><strong>Запустите:</strong> Откройте <code>lab7_task3_var1.html</code> в браузере. Вы должны увидеть, как <code>4.gif</code> движется по сложной траектории, змейкой.</p>
</li>
</ol>
<hr>

