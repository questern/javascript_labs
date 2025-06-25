---


---

<p>Я не могу выполнить все задания из лабораторных работ, так как для этого мне бы понадобился доступ к интерактивной среде разработки (IDE) и возможность выполнять JavaScript-код, а также создавать и изменять HTML-файлы. Мои возможности ограничены текстовым форматом ответа.</p>
<p>Однако я могу проанализировать предоставленные страницы и <strong>предложить решения или объяснить подходы к выполнению каждого задания</strong>, основываясь на том, что есть в пособии. Вы сможете использовать эти объяснения для самостоятельной работы.</p>
<p>Давайте пройдемся по заданиям, используя информацию из учебного пособия.</p>
<hr>
<h3 id="ф.в.-филиппов-технологии-обработки-информации-часть-1-javascript"><strong>Ф.В. Филиппов “ТЕХНОЛОГИИ ОБРАБОТКИ ИНФОРМАЦИИ” Часть 1 (JavaScript)</strong></h3>
<hr>
<h3 id="лабораторная-работа-№-1-введение-в-javascript"><strong>ЛАБОРАТОРНАЯ РАБОТА № 1: Введение в JavaScript</strong></h3>
<p><strong>Цель:</strong> Научиться подключать JavaScript к странице и использовать базовые функции ввода/вывода (alert, confirm, prompt).</p>
<p><strong>Задание 1 (Вариант 1):</strong><br>
Введите свою фамилию, имя и отчество. Запросите подтверждение. Если все верно, то вывести приветствие, если нет, вывести сообщение об ошибке.</p>
<p><strong>Пояснение и подход:</strong></p>
<ol>
<li><strong>Ввод:</strong> Используйте функцию <code>prompt()</code> для поочередного ввода фамилии, имени и отчества. Сохраняйте каждое значение в отдельную переменную.
<ul>
<li>Пример: <code>var surname = prompt("Введите свою фамилию:", "Иванов");</code></li>
</ul>
</li>
<li><strong>Подтверждение:</strong> Сформируйте строку-сообщение для <code>confirm()</code>, объединив введенные ФИО.
<ul>
<li>Пример: <code>var confirmation = confirm("ФИО: " + surname + " " + name + " " + patronymic + "\nВсе верно?");</code></li>
</ul>
</li>
<li><strong>Обработка подтверждения:</strong> Используйте условный оператор <code>if...else</code> для проверки результата <code>confirm()</code>.
<ul>
<li>Если <code>confirm()</code> вернул <code>true</code> (нажата “ОК”): Используйте <code>alert()</code> для вывода приветствия, например, "Молодец, " + ФИО.</li>
<li>Если <code>confirm()</code> вернул <code>false</code> (нажата “Отмена”): Используйте <code>alert()</code> для вывода сообщения об ошибке, например, “Ошибка в данных”.</li>
</ul>
</li>
<li><strong>HTML-структура:</strong> JavaScript-код можно разместить в теге <code>&lt;script&gt;</code> внутри <code>&lt;body&gt;</code> или <code>&lt;head&gt;</code>. Для простых последовательных действий без обработчиков событий, можно разместить прямо в <code>&lt;body&gt;</code>.</li>
</ol>
<p><strong>Примерный JavaScript-код:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Лаб. работа 1 - Задание 1<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/javascript<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> surname <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свою фамилию:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> name <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите Ваше имя:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> patronymic <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите Ваше отчество:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">var</span> full_name <span class="token operator">=</span> surname <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> name <span class="token operator">+</span> <span class="token string">" "</span> <span class="token operator">+</span> patronymic<span class="token punctuation">;</span>

        <span class="token keyword">var</span> isCorrect <span class="token operator">=</span> <span class="token function">confirm</span><span class="token punctuation">(</span><span class="token string">"ФИО: "</span> <span class="token operator">+</span> full_name <span class="token operator">+</span> <span class="token string">"\nВсе верно?"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">if</span> <span class="token punctuation">(</span>isCorrect<span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Молодец, "</span> <span class="token operator">+</span> full_name<span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка в данных"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>

<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<hr>
<p><strong>Задание 2 (Вариант 1):</strong><br>
Введите время в часах и минутах. Определите время, которое будет через минуту. Используйте вложенные операторы IF. Возможны три случая:</p>
<ol>
<li>Минуты &lt; 59 (просто увеличиваются минуты)</li>
<li>Минуты = 59, часы &lt; 23 (минуты обнуляются, часы увеличиваются)</li>
<li>Минуты = 59, часы = 23 (минуты и часы обнуляются)</li>
</ol>
<p><strong>Пояснение и подход:</strong></p>
<ol>
<li><strong>Ввод:</strong> Используйте <code>prompt()</code> для ввода часов и минут. Важно преобразовать введенные строковые значения в числа с помощью <code>parseInt()</code>.
<ul>
<li>Пример: <code>var hours = parseInt(prompt("Введите количество часов:", "0"));</code></li>
</ul>
</li>
<li><strong>Обработка логики:</strong>
<ul>
<li>Увеличьте минуты на 1: <code>minutes++</code>.</li>
<li>Используйте <code>if</code> для проверки, не превысили ли минуты 59: <code>if (minutes &gt;= 60)</code>. Если превысили:
<ul>
<li>Обнулите минуты: <code>minutes = 0;</code></li>
<li>Увеличьте часы на 1: <code>hours++;</code></li>
<li>Используйте вложенный <code>if</code> для проверки, не превысили ли часы 23: <code>if (hours &gt;= 24)</code>. Если превысили:
<ul>
<li>Обнулите часы: <code>hours = 0;</code></li>
</ul>
</li>
</ul>
</li>
</ul>
</li>
<li><strong>Вывод:</strong> Используйте <code>alert()</code> для отображения нового времени.</li>
</ol>
<p><strong>Примерный JavaScript-код:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Лаб. работа 1 - Задание 2<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/javascript<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> hours <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span><span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите количество часов:"</span><span class="token punctuation">,</span> <span class="token string">"14"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> minutes <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span><span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите количество минут:"</span><span class="token punctuation">,</span> <span class="token string">"35"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        minutes<span class="token operator">++</span><span class="token punctuation">;</span> <span class="token comment">// Увеличиваем минуты на 1</span>

        <span class="token keyword">if</span> <span class="token punctuation">(</span>minutes <span class="token operator">&gt;=</span> <span class="token number">60</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            minutes <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Обнуляем минуты, если достигли 60</span>
            hours<span class="token operator">++</span><span class="token punctuation">;</span>     <span class="token comment">// Увеличиваем часы</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>hours <span class="token operator">&gt;=</span> <span class="token number">24</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                hours <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Обнуляем часы, если достигли 24</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>

        <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Через минуту будет "</span> <span class="token operator">+</span> hours <span class="token operator">+</span> <span class="token string">" час и "</span> <span class="token operator">+</span> minutes <span class="token operator">+</span> <span class="token string">" мин"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>

<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<hr>
<p><strong>Задание 3 (Вариант 1 - Шахматный порядок с использованием CSS классов):</strong><br>
Создадим таблицу 10 на 10. Высота и ширина ячейки 50 пикселей. Закрасим таблицу в шахматном порядке. Таблицу будем формировать динамически, с помощью метода write. Для закраски таблицы используем вложенные операторы цикла.</p>
<p><strong>Пояснение и подход:</strong></p>
<ol>
<li><strong>CSS-стили:</strong> Создайте внешний CSS-файл (например, <code>1.css</code>) или встройте стили в <code>&lt;head&gt;</code> для определения классов <code>r1</code> (красный) и <code>r2</code> (синий), а также стили для таблицы и ячеек.
<ul>
<li><code>table { border-collapse: collapse; }</code></li>
<li><code>td { width: 50px; height: 50px; }</code></li>
<li><code>.r1 { background-color: red; }</code></li>
<li><code>.r2 { background-color: blue; }</code></li>
</ul>
</li>
<li><strong>HTML-структура:</strong> В <code>&lt;body&gt;</code> будет скрипт, который динамически формирует таблицу.</li>
<li><strong>Динамическое формирование таблицы:</strong>
<ul>
<li>Используйте <code>document.write("&lt;table&gt;");</code> в начале и <code>document.write("&lt;/table&gt;");</code> в конце.</li>
<li>Внешний цикл <code>for</code> (например, <code>i</code> от 1 до 10) для строк: <code>document.write("&lt;tr&gt;");</code> и <code>document.write("&lt;/tr&gt;");</code>.</li>
<li>Внутренний цикл <code>for</code> (например, <code>j</code> от 1 до 10) для столбцов: <code>document.write("&lt;td "+s+"&gt; &lt;/td&gt;");</code></li>
<li><strong>Шахматный порядок:</strong> Определите, какой класс (r1 или r2) присвоить ячейке. Наиболее распространенный способ - проверять четность суммы индексов строки и столбца <code>(i + j) % 2</code>.
<ul>
<li>Если <code>(i + j) % 2 == 0</code>, то одна заливка (например, <code>r1</code>).</li>
<li>Если <code>(i + j) % 2 != 0</code>, то другая заливка (например, <code>r2</code>).</li>
<li>Переменная <code>s</code> будет содержать <code>class='r1'</code> или <code>class='r2'</code>.</li>
</ul>
</li>
</ul>
</li>
</ol>
<p><strong>Примерный JavaScript-код и CSS:</strong></p>
<p><strong><code>1.css</code>:</strong></p>
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
<p><strong><code>html</code> файл:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Лаб. работа 1 - Задание 3<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>link</span> <span class="token attr-name">rel</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>stylesheet<span class="token punctuation">"</span></span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/css<span class="token punctuation">"</span></span> <span class="token attr-name">href</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>1.css<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/javascript<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> n <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span> <span class="token comment">// Размер таблицы</span>
        <span class="token keyword">var</span> s<span class="token punctuation">;</span> <span class="token comment">// Для хранения класса</span>

        document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;table&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">var</span> i <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> i <span class="token operator">&lt;=</span> n<span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;tr&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Начало строки</span>
            <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">var</span> j <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> j <span class="token operator">&lt;=</span> n<span class="token punctuation">;</span> j<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token comment">// Определяем класс для ячейки в шахматном порядке</span>
                <span class="token keyword">var</span> st <span class="token operator">=</span> <span class="token punctuation">(</span>i <span class="token operator">+</span> j<span class="token punctuation">)</span> <span class="token operator">%</span> <span class="token number">2</span><span class="token punctuation">;</span>
                <span class="token keyword">if</span> <span class="token punctuation">(</span>st <span class="token operator">===</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    s <span class="token operator">=</span> <span class="token string">"class='r1'"</span><span class="token punctuation">;</span> <span class="token comment">// Красный</span>
                <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                    s <span class="token operator">=</span> <span class="token string">"class='r2'"</span><span class="token punctuation">;</span> <span class="token comment">// Синий</span>
                <span class="token punctuation">}</span>
                document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;td "</span> <span class="token operator">+</span> s <span class="token operator">+</span> <span class="token string">"&gt; &lt;/td&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Добавляем ячейку</span>
            <span class="token punctuation">}</span>
            document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;/tr&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Конец строки</span>
        <span class="token punctuation">}</span>

        document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;/table&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>

<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<hr>
<h3 id="лабораторная-работа-№-2-события-и-функции"><strong>ЛАБОРАТОРНАЯ РАБОТА № 2: События и функции</strong></h3>
<p><strong>Цель:</strong> Изучить события JavaScript и использование функций для организации кода.</p>
<p><strong>Задание:</strong><br>
Оформить задание 2 из Лабораторной работы 1 в виде функции и вызвать эту функцию по нажатию кнопки.</p>
<p><strong>Пояснение и подход:</strong><br>
Задание 2 из Лабораторной работы 1 касалось определения времени через минуту. Теперь эту логику нужно обернуть в функцию и вызывать её по событию <code>onclick</code> кнопки.</p>
<ol>
<li><strong>HTML-структура:</strong>
<ul>
<li>Создайте кнопку <code>&lt;input type="button" value="Посчитать время" onclick="calculateTime();"&gt;</code>. Атрибут <code>onclick</code> будет вызывать функцию <code>calculateTime()</code>.</li>
<li>JavaScript-код с функцией поместите в <code>&lt;script&gt;</code> тег внутри <code>&lt;head&gt;</code> (лучшая практика для функций).</li>
</ul>
</li>
<li><strong>Функция:</strong>
<ul>
<li>Создайте функцию, например, <code>calculateTime()</code>.</li>
<li>Вся логика из Задания 2 Лабораторной работы 1 (prompt для часов/минут, инкремент минут/часов, alert) должна быть внутри этой функции.</li>
</ul>
</li>
</ol>
<p><strong>Примерный JavaScript-код:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Лаб. работа 2 - Задание<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/javascript<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">calculateTime</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> hours <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span><span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите количество часов:"</span><span class="token punctuation">,</span> <span class="token string">"14"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> minutes <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span><span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите количество минут:"</span><span class="token punctuation">,</span> <span class="token string">"35"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token comment">// Проверяем, что введены корректные числа</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>hours<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>minutes<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Пожалуйста, введите числа для часов и минут."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                <span class="token keyword">return</span><span class="token punctuation">;</span> <span class="token comment">// Выходим из функции</span>
            <span class="token punctuation">}</span>

            minutes<span class="token operator">++</span><span class="token punctuation">;</span> <span class="token comment">// Увеличиваем минуты на 1</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>minutes <span class="token operator">&gt;=</span> <span class="token number">60</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                minutes <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Обнуляем минуты, если достигли 60</span>
                hours<span class="token operator">++</span><span class="token punctuation">;</span>     <span class="token comment">// Увеличиваем часы</span>

                <span class="token keyword">if</span> <span class="token punctuation">(</span>hours <span class="token operator">&gt;=</span> <span class="token number">24</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    hours <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Обнуляем часы, если достигли 24</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">}</span>

            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Через минуту будет "</span> <span class="token operator">+</span> hours <span class="token operator">+</span> <span class="token string">" час и "</span> <span class="token operator">+</span> minutes <span class="token operator">+</span> <span class="token string">" мин"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span>Определение времени через минуту<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">onclick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>calculateTime()<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Посчитать время через минуту<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
    <span class="token comment">&lt;!-- Или input type="button" как в пособии --&gt;</span>
    <span class="token comment">&lt;!-- &lt;input type="button" value="Посчитать время" onclick="calculateTime()"&gt; --&gt;</span>

<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<hr>
<h3 id="лабораторная-работа-№-3-встроенные-объекты"><strong>ЛАБОРАТОРНАЯ РАБОТА № 3: Встроенные объекты</strong></h3>
<p><strong>Цель:</strong> Изучить базовые встроенные объекты JavaScript (Math, Date, Array) и использование <code>document.getElementById()</code>.</p>
<p><strong>Вариант 2 - Задание 1:</strong><br>
Введите свою фамилию, пол и возраст. Запросите подтверждение. Если все верно, то вывести приветствие, если нет, вывести сообщение об ошибке. (Аналогично Заданию 1 Лаб.1, но с другими данными).</p>
<p><strong>Пояснение и подход:</strong><br>
Повторение Задания 1 Лаб.1 с изменением запрашиваемых данных (фамилия, пол, возраст). Логика <code>prompt</code>, <code>confirm</code>, <code>alert</code> остается той же.</p>
<p><strong>Примерный JavaScript-код:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Лаб. работа 3 - Задание 1 (Вариант 2)<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/javascript<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> surname <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свою фамилию:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> gender <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свой пол (м/ж):"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> age <span class="token operator">=</span> <span class="token function">parseInt</span><span class="token punctuation">(</span><span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите свой возраст:"</span><span class="token punctuation">,</span> <span class="token string">""</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token comment">// Проверка на число для возраста</span>
        <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>age<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
             <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Возраст должен быть числом."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
             <span class="token comment">// Можно попросить ввести заново или выйти</span>
             <span class="token comment">// return;</span>
        <span class="token punctuation">}</span>

        <span class="token keyword">var</span> confirmation <span class="token operator">=</span> <span class="token function">confirm</span><span class="token punctuation">(</span>
            <span class="token string">"ФИО: "</span> <span class="token operator">+</span> surname <span class="token operator">+</span> <span class="token string">"\n"</span> <span class="token operator">+</span>
            <span class="token string">"Пол: "</span> <span class="token operator">+</span> gender <span class="token operator">+</span> <span class="token string">"\n"</span> <span class="token operator">+</span>
            <span class="token string">"Возраст: "</span> <span class="token operator">+</span> age <span class="token operator">+</span> <span class="token string">"\n"</span> <span class="token operator">+</span>
            <span class="token string">"Все верно?"</span>
        <span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">if</span> <span class="token punctuation">(</span>confirmation<span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Молодец, "</span> <span class="token operator">+</span> surname<span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка в данных"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>

<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<hr>
<p><strong>Вариант 2 - Задание 2:</strong><br>
Дано два числа х, у и знак арифметической операции (+, -, *, /). Найти х+у, x-y, x*y, х/у, в зависимости от введенного знака. В случае ошибки в знаке или деления на 0 вывести сообщение об ошибке.</p>
<p><strong>Пояснение и подход:</strong></p>
<ol>
<li><strong>Ввод:</strong> Три <code>prompt()</code> для двух чисел (<code>x</code>, <code>y</code>) и знака операции (<code>op</code>). Преобразуйте <code>x</code> и <code>y</code> в числа с помощью <code>parseFloat()</code> или <code>parseInt()</code>.</li>
<li><strong>Обработка операции:</strong> Используйте <code>if-else if-else</code> для проверки знака операции.
<ul>
<li>Проверьте деление на ноль: если знак <code>/</code> и <code>y === 0</code>, выведите ошибку.</li>
<li>Используйте <code>alert()</code> для вывода результата или сообщения об ошибке.</li>
</ul>
</li>
</ol>
<p><strong>Примерный JavaScript-код:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Лаб. работа 3 - Задание 2 (Вариант 2)<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/javascript<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> num1 <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span><span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите первое число:"</span><span class="token punctuation">,</span> <span class="token string">"45"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> num2 <span class="token operator">=</span> <span class="token function">parseFloat</span><span class="token punctuation">(</span><span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите второе число:"</span><span class="token punctuation">,</span> <span class="token string">"15"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> operation <span class="token operator">=</span> <span class="token function">prompt</span><span class="token punctuation">(</span><span class="token string">"Введите знак арифметической операции (+, -, *, /):"</span><span class="token punctuation">,</span> <span class="token string">"+"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> result<span class="token punctuation">;</span>

        <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token function">isNaN</span><span class="token punctuation">(</span>num1<span class="token punctuation">)</span> <span class="token operator">||</span> <span class="token function">isNaN</span><span class="token punctuation">(</span>num2<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Введите числовые значения."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
            <span class="token keyword">switch</span> <span class="token punctuation">(</span>operation<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token keyword">case</span> <span class="token string">'+'</span><span class="token punctuation">:</span>
                    result <span class="token operator">=</span> num1 <span class="token operator">+</span> num2<span class="token punctuation">;</span>
                    <span class="token function">alert</span><span class="token punctuation">(</span>num1 <span class="token operator">+</span> <span class="token string">" + "</span> <span class="token operator">+</span> num2 <span class="token operator">+</span> <span class="token string">" = "</span> <span class="token operator">+</span> result<span class="token punctuation">)</span><span class="token punctuation">;</span>
                    <span class="token keyword">break</span><span class="token punctuation">;</span>
                <span class="token keyword">case</span> <span class="token string">'-'</span><span class="token punctuation">:</span>
                    result <span class="token operator">=</span> num1 <span class="token operator">-</span> num2<span class="token punctuation">;</span>
                    <span class="token function">alert</span><span class="token punctuation">(</span>num1 <span class="token operator">+</span> <span class="token string">" - "</span> <span class="token operator">+</span> num2 <span class="token operator">+</span> <span class="token string">" = "</span> <span class="token operator">+</span> result<span class="token punctuation">)</span><span class="token punctuation">;</span>
                    <span class="token keyword">break</span><span class="token punctuation">;</span>
                <span class="token keyword">case</span> <span class="token string">'*'</span><span class="token punctuation">:</span>
                    result <span class="token operator">=</span> num1 <span class="token operator">*</span> num2<span class="token punctuation">;</span>
                    <span class="token function">alert</span><span class="token punctuation">(</span>num1 <span class="token operator">+</span> <span class="token string">" * "</span> <span class="token operator">+</span> num2 <span class="token operator">+</span> <span class="token string">" = "</span> <span class="token operator">+</span> result<span class="token punctuation">)</span><span class="token punctuation">;</span>
                    <span class="token keyword">break</span><span class="token punctuation">;</span>
                <span class="token keyword">case</span> <span class="token string">'/'</span><span class="token punctuation">:</span>
                    <span class="token keyword">if</span> <span class="token punctuation">(</span>num2 <span class="token operator">===</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                        <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Деление на ноль невозможно."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
                    <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                        result <span class="token operator">=</span> num1 <span class="token operator">/</span> num2<span class="token punctuation">;</span>
                        <span class="token function">alert</span><span class="token punctuation">(</span>num1 <span class="token operator">+</span> <span class="token string">" / "</span> <span class="token operator">+</span> num2 <span class="token operator">+</span> <span class="token string">" = "</span> <span class="token operator">+</span> result<span class="token punctuation">)</span><span class="token punctuation">;</span>
                    <span class="token punctuation">}</span>
                    <span class="token keyword">break</span><span class="token punctuation">;</span>
                <span class="token keyword">default</span><span class="token punctuation">:</span>
                    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Ошибка: Неизвестная операция."</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>

<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<hr>
<p><strong>Вариант 2 - Задание 3:</strong><br>
(Шахматная доска с другими цветами или немного измененным узором - картинка демонстрирует диагональный шахматный порядок).</p>
<p><strong>Пояснение и подход:</strong><br>
Повторение Задания 3 Лаб.1, но с изменением цветов или логики определения класса для ячейки, чтобы получить другой узор. В данном случае, на картинке, похоже, используется <code>(i % 2 === 0 &amp;&amp; j % 2 === 0) || (i % 2 !== 0 &amp;&amp; j % 2 !== 0)</code> для одного цвета и <code>(i % 2 === 0 &amp;&amp; j % 2 !== 0) || (i % 2 !== 0 &amp;&amp; j % 2 === 0)</code> для другого, что дает классический шахматный порядок. Если нужен именно диагональный, как на примере, то можно попробовать комбинировать условия четности, как <code>(i + j) % 2</code> (классический) или <code>(i - j) % 2</code> (для диагоналей). В примере на картинке, кажется, использована несколько иная логика. Давайте сделаем классический, но с предложенными цветами.</p>
<p>Если на картинке узор скорее похож на диагональные полосы (или “полосы”), то можно попробовать <code>i % 2</code> или <code>j % 2</code> или <code>(i + j) % 3</code> и т.п.</p>
<p>Примем, что требуется просто стандартный шахматный порядок с оранжевым и синим цветами (судя по одному из квадратов).<br>
Цвета из картинки: синий и оранжевый/бирюзовый. Допустим, <code>lightblue</code> и <code>darkblue</code>.</p>
<p><strong><code>1.css</code> (обновленный):</strong></p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">table </span><span class="token punctuation">{</span>
    <span class="token property">border-collapse</span><span class="token punctuation">:</span> collapse<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token selector">td </span><span class="token punctuation">{</span>
    <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">50</span>px<span class="token punctuation">;</span>
    <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">50</span>px<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token selector"><span class="token class">.color1</span> </span><span class="token punctuation">{</span>
    <span class="token property">background-color</span><span class="token punctuation">:</span> lightblue<span class="token punctuation">;</span> <span class="token comment">/* Светлый цвет */</span>
<span class="token punctuation">}</span>
<span class="token selector"><span class="token class">.color2</span> </span><span class="token punctuation">{</span>
    <span class="token property">background-color</span><span class="token punctuation">:</span> darkblue<span class="token punctuation">;</span>  <span class="token comment">/* Темный цвет */</span>
<span class="token punctuation">}</span>
</code></pre>
<p><strong><code>html</code> файл (обновленный):</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Лаб. работа 3 - Задание 3 (Вариант 2)<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>link</span> <span class="token attr-name">rel</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>stylesheet<span class="token punctuation">"</span></span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/css<span class="token punctuation">"</span></span> <span class="token attr-name">href</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>1.css<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/javascript<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> n <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> s<span class="token punctuation">;</span>

        document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;table&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">var</span> i <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> i <span class="token operator">&lt;=</span> n<span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;tr&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">var</span> j <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> j <span class="token operator">&lt;=</span> n<span class="token punctuation">;</span> j<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token comment">// Классический шахматный порядок</span>
                <span class="token keyword">var</span> cell_type <span class="token operator">=</span> <span class="token punctuation">(</span>i <span class="token operator">+</span> j<span class="token punctuation">)</span> <span class="token operator">%</span> <span class="token number">2</span><span class="token punctuation">;</span>
                <span class="token keyword">if</span> <span class="token punctuation">(</span>cell_type <span class="token operator">===</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    s <span class="token operator">=</span> <span class="token string">"class='color1'"</span><span class="token punctuation">;</span> <span class="token comment">// Светлый цвет</span>
                <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                    s <span class="token operator">=</span> <span class="token string">"class='color2'"</span><span class="token punctuation">;</span> <span class="token comment">// Темный цвет</span>
                <span class="token punctuation">}</span>
                document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;td "</span> <span class="token operator">+</span> s <span class="token operator">+</span> <span class="token string">"&gt; &lt;/td&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;/tr&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>

        document<span class="token punctuation">.</span><span class="token function">write</span><span class="token punctuation">(</span><span class="token string">"&lt;/table&gt;"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<hr>
<h3 id="лабораторная-работа-№-4-объект-window"><strong>ЛАБОРАТОРНАЯ РАБОТА № 4: Объект Window</strong></h3>
<p><strong>Цель:</strong> Изучить работу с окнами браузера (<code>open()</code>, <code>close()</code>), динамическое формирование содержимого.</p>
<p><strong>Вариант 1 - Задание 1:</strong><br>
Создайте документ, в котором рисунок <code>neznakomka3.jpg</code> заключен в рамку серого цвета типа <code>inset</code> и толщиной 50. По нажатию кнопки изменять цвет рамки на синий и надпись на кнопке. При следующем нажатии изменять цвет рамки на серый и надпись на кнопке.</p>
<p><strong>Пояснение и подход:</strong><br>
Это задание включает изменение стилей элемента по кнопке, что скорее относится к Лабораторной работе № 7 (свойство <code>style</code>). Однако, поскольку это в Лаб.4, возможно, есть скрытый подвох с использованием <code>window</code> или <code>document</code>, но прямого указания нет. Будем использовать изменение <code>style</code> элемента.</p>
<ol>
<li><strong>HTML-структура:</strong>
<ul>
<li><code>&lt;img&gt;</code> с <code>id</code> для рисунка.</li>
<li><code>&lt;button&gt;</code> с <code>onclick</code> для вызова функции.</li>
<li>Возможно, <code>div</code> вокруг изображения для рамки или стилизировать само изображение. Стиль <code>border</code> для изображения.</li>
</ul>
</li>
<li><strong>JavaScript-функция:</strong>
<ul>
<li>Должна получить доступ к элементу <code>img</code> по его <code>id</code> с помощью <code>document.getElementById()</code>.</li>
<li>Использовать внутреннюю переменную-флаг (например, <code>isBlue</code>) для отслеживания текущего состояния цвета рамки.</li>
<li>При каждом вызове функции:
<ul>
<li>Проверять флаг.</li>
<li>В зависимости от флага, менять <code>img.style.borderColor</code> на синий или серый, <code>img.style.borderStyle</code> на <code>inset</code>, <code>img.style.borderWidth</code> на <code>50px</code>.</li>
<li>Менять <code>value</code> или <code>textContent</code> кнопки.</li>
<li>Изменять значение флага.</li>
</ul>
</li>
</ul>
</li>
</ol>
<p><strong>Примерный JavaScript-код и CSS (если используется внешний файл):</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Лаб. работа 4 - Задание 1<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token comment">/* Изображение будет стилизовано JS, но можно задать начальные стили здесь */</span>
        <span class="token selector"><span class="token id">#myImage</span> </span><span class="token punctuation">{</span>
            <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">50</span>px inset gray<span class="token punctuation">;</span> <span class="token comment">/* Начальный серый цвет */</span>
            <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span> <span class="token comment">/* Чтобы рамка корректно отображалась */</span>
            <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span> <span class="token comment">/* Центрирование */</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>myImage<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>neznakomka3.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Незнакомка<span class="token punctuation">"</span></span><span class="token style-attr language-css"><span class="token attr-name"> <span class="token attr-name">style</span></span><span class="token punctuation">="</span><span class="token attr-value"><span class="token property">width</span><span class="token punctuation">:</span><span class="token number">300</span>px<span class="token punctuation">;</span> <span class="token property">height</span><span class="token punctuation">:</span>auto<span class="token punctuation">;</span></span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>colorChangeButton<span class="token punctuation">"</span></span> <span class="token attr-name">onclick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>changeBorderColor()<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Изменить рамку на синий<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/javascript<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token comment">// Переменная-флаг для отслеживания текущего цвета рамки (true - синий, false - серый)</span>
        <span class="token keyword">var</span> isBlue <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span> <span class="token comment">// Начинаем с серого цвета, как в HTML/CSS</span>

        <span class="token keyword">function</span> <span class="token function">changeBorderColor</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> image <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'myImage'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> button <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'colorChangeButton'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>isBlue<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token comment">// Если сейчас синий, меняем на серый</span>
                image<span class="token punctuation">.</span>style<span class="token punctuation">.</span>borderColor <span class="token operator">=</span> <span class="token string">'gray'</span><span class="token punctuation">;</span>
                button<span class="token punctuation">.</span>textContent <span class="token operator">=</span> <span class="token string">'Изменить рамку на синий'</span><span class="token punctuation">;</span>
                isBlue <span class="token operator">=</span> <span class="token boolean">false</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token comment">// Если сейчас серый, меняем на синий</span>
                image<span class="token punctuation">.</span>style<span class="token punctuation">.</span>borderColor <span class="token operator">=</span> <span class="token string">'blue'</span><span class="token punctuation">;</span>
                button<span class="token punctuation">.</span>textContent <span class="token operator">=</span> <span class="token string">'Изменить рамку на серый'</span><span class="token punctuation">;</span>
                isBlue <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
            image<span class="token punctuation">.</span>style<span class="token punctuation">.</span>borderStyle <span class="token operator">=</span> <span class="token string">'inset'</span><span class="token punctuation">;</span> <span class="token comment">// Убедиться, что стиль не меняется</span>
            image<span class="token punctuation">.</span>style<span class="token punctuation">.</span>borderWidth <span class="token operator">=</span> <span class="token string">'50px'</span><span class="token punctuation">;</span>   <span class="token comment">// Убедиться, что ширина не меняется</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>

<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p>Не забудьте поместить изображение <code>neznakomka3.jpg</code> в ту же папку, что и HTML-файл, или указать правильный путь к нему. Если у вас нет этого изображения, используйте любое другое.</p>
<hr>
<p><strong>Вариант 1 - Задание 2:</strong><br>
Сначала на странице только текст стихотворения и кнопка с надписью «показать свечу». При нажатии на кнопку текст стихотворения прячется, на его месте появляется рисунок, и надпись на кнопке меняется на «показать текст». Если еще раз нажать на кнопку, рисунок исчезает и появляется текст.<br>
<em>Параметры форматирования страницы:</em> (некоторые из них будут заданы статически в CSS, другие динамически через JS)</p>
<ul>
<li>Цвет фона темно-синий</li>
<li>Размер шрифта 22, курсив, цвет шрифта белый</li>
<li>Рамка вокруг текста: цвет <code>#ffA089</code>, тип <code>outset</code>, толщина 5.</li>
<li>Картинка размером 200 на 200.</li>
<li>Рамка вокруг картинки: цвет <code>#ffA089</code>, тип <code>outset</code>, толщина 50, отступы по 5.</li>
</ul>
<p><strong>Пояснение и подход:</strong><br>
Это задание требует динамического скрытия/отображения элементов и изменения их стилей.</p>
<ol>
<li>
<p><strong>HTML-структура:</strong></p>
<ul>
<li><code>div</code> для стихотворения (с <code>id</code>)</li>
<li><code>img</code> для свечи (с <code>id</code> и <code>display: none</code> изначально)</li>
<li><code>&lt;button&gt;</code> с <code>onclick</code> и <code>id</code>.</li>
<li>Текст стихотворения поместите в <code>id="poem"</code>.</li>
<li>Изображение свечи поместите в <code>id="candleImage"</code>.</li>
</ul>
</li>
<li>
<p><strong>CSS-стили:</strong> Задайте начальные стили для <code>body</code>, абзацев/div с текстом, и изображения (рамки, размер). Изначально изображение должно быть <code>display: none;</code>.</p>
</li>
<li>
<p><strong>JavaScript-функция (<code>toggleContent()</code>):</strong></p>
<ul>
<li>Получите ссылки на <code>div</code> с текстом, <code>img</code> с свечой и кнопку.</li>
<li>Используйте флаг или проверьте <code>display</code> свойство <code>poem</code> (или <code>candleImage</code>) чтобы определить, что сейчас отображается.</li>
<li>Если отображается текст:
<ul>
<li>Скрыть текст (<code>poem.style.display = 'none';</code>).</li>
<li>Показать изображение (<code>candleImage.style.display = 'block';</code>).</li>
<li>Установить стили рамки для изображения.</li>
<li>Изменить текст кнопки на “Показать текст”.</li>
</ul>
</li>
<li>Если отображается изображение:
<ul>
<li>Скрыть изображение (<code>candleImage.style.display = 'none';</code>).</li>
<li>Показать текст (<code>poem.style.display = 'block';</code>).</li>
<li>Изменить текст кнопки на “Показать свечу”.</li>
</ul>
</li>
</ul>
</li>
</ol>
<p><strong>Примерный JavaScript-код и CSS:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Лаб. работа 4 - Задание 2<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span>
            <span class="token property">background-color</span><span class="token punctuation">:</span> darkblue<span class="token punctuation">;</span> <span class="token comment">/* Темно-синий фон */</span>
            <span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span>             <span class="token comment">/* Белый шрифт */</span>
            <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">22</span>px<span class="token punctuation">;</span>
            <span class="token property">font-style</span><span class="token punctuation">:</span> italic<span class="token punctuation">;</span>       <span class="token comment">/* Курсив */</span>
            <span class="token property">font-family</span><span class="token punctuation">:</span> sans-serif<span class="token punctuation">;</span>  <span class="token comment">/* Для примера */</span>
            <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#poem</span> </span><span class="token punctuation">{</span>
            <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">5</span>px outset <span class="token hexcode">#ffA089</span><span class="token punctuation">;</span> <span class="token comment">/* Рамка вокруг текста */</span>
            <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span>
            <span class="token property">margin-bottom</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span>
            <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span> <span class="token comment">/* Чтобы padding не увеличивал размер */</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#candleImage</span> </span><span class="token punctuation">{</span>
            <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">200</span>px<span class="token punctuation">;</span>
            <span class="token property">height</span><span class="token punctuation">:</span> <span class="token number">200</span>px<span class="token punctuation">;</span>
            <span class="token property">display</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span>           <span class="token comment">/* Изначально скрыто */</span>
            <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">50</span>px outset <span class="token hexcode">#ffA089</span><span class="token punctuation">;</span> <span class="token comment">/* Рамка вокруг картинки */</span>
            <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span>              <span class="token comment">/* Отступы по 5 */</span>
            <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span>         <span class="token comment">/* Центрирование */</span>
            <span class="token property">box-sizing</span><span class="token punctuation">:</span> border-box<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector">button </span><span class="token punctuation">{</span>
            <span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span>
            <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">20</span>px auto<span class="token punctuation">;</span>
            <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">20</span>px<span class="token punctuation">;</span>
            <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">18</span>px<span class="token punctuation">;</span>
            <span class="token property">cursor</span><span class="token punctuation">:</span> pointer<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>poem<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span>Иннокентий Анненский<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span>
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

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>candleImage<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>свеча1.gif<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Свеча<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggleButton<span class="token punctuation">"</span></span> <span class="token attr-name">onclick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>toggleContent()<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Показать свечу<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/javascript<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">function</span> <span class="token function">toggleContent</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">var</span> poemDiv <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'poem'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> candleImg <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'candleImage'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token keyword">var</span> toggleBtn <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'toggleButton'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

            <span class="token keyword">if</span> <span class="token punctuation">(</span>poemDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">===</span> <span class="token string">'none'</span> <span class="token operator">||</span> poemDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">===</span> <span class="token string">''</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Если текст скрыт или не задан (т.е. по умолчанию block)</span>
                <span class="token comment">// Скрываем текст, показываем картинку</span>
                poemDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'block'</span><span class="token punctuation">;</span> <span class="token comment">// Показываем текст</span>
                candleImg<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'none'</span><span class="token punctuation">;</span> <span class="token comment">// Скрываем картинку</span>
                toggleBtn<span class="token punctuation">.</span>textContent <span class="token operator">=</span> <span class="token string">'Показать свечу'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                <span class="token comment">// Скрываем картинку, показываем текст</span>
                poemDiv<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'none'</span><span class="token punctuation">;</span> <span class="token comment">// Скрываем текст</span>
                candleImg<span class="token punctuation">.</span>style<span class="token punctuation">.</span>display <span class="token operator">=</span> <span class="token string">'block'</span><span class="token punctuation">;</span> <span class="token comment">// Показываем картинку</span>
                toggleBtn<span class="token punctuation">.</span>textContent <span class="token operator">=</span> <span class="token string">'Показать текст'</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>

        <span class="token comment">// Если вы хотите, чтобы изначально отображалась кнопка "Показать свечу",</span>
        <span class="token comment">// а текст был виден, то эта функция будет вызываться при первой загрузке или клике.</span>
        <span class="token comment">// Чтобы текст был изначально виден, а картинка скрыта, не нужно дополнительных вызовов тут,</span>
        <span class="token comment">// достаточно CSS.</span>
        <span class="token comment">// Если вы хотите ИНАЧЕ, например чтобы сначала была картинка скрыта, тогда:</span>
        <span class="token comment">// window.onload = function() { toggleContent(); };</span>
        <span class="token comment">// или установить poemDiv.style.display = 'block' и candleImg.style.display = 'none' явно.</span>
        <span class="token comment">// В текущем коде HTML/CSS `poem` виден, `candleImage` скрыт. Кнопка "Показать свечу".</span>
        <span class="token comment">// При первом клике текст скроется, свеча появится, текст кнопки поменяется на "Показать текст".</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p>Замените <code>свеча1.gif</code> на реальное изображение или путь к нему. Для текста можете скопировать приведенный.</p>
<hr>
<p><strong>Вариант 1 - Задание 3:</strong><br>
Создайте документ, в котором рисунок <code>p5_0.jpg</code> занимает 50% окна и является нижним слоем. На верхнем слое второй рисунок <code>4.gif</code>, который двигается по горизонтали к правой границе первого рисунка, затем на строку (высоту рисунка) вниз и назад, к левой границе, на строку вниз и к правой границе, и т.д. до нижней границы первого рисунка.</p>
<p><strong>Пояснение и подход:</strong><br>
Это задание на анимацию. Вам нужно будет использовать <code>position: absolute</code>, <code>left</code>, <code>top</code> для движения и <code>setTimeout</code> для цикличной анимации.</p>
<ol>
<li><strong>HTML-структура:</strong> Два изображения с <code>id</code>. Одно <code>p5_0.jpg</code> как фон/нижний слой, другое <code>4.gif</code> как анимированный элемент.</li>
<li><strong>CSS-стили:</strong>
<ul>
<li><code>p5_0.jpg</code>: <code>width: 50%; position: absolute; top: 0; left: 0; z-index: 1;</code>.</li>
<li><code>4.gif</code>: <code>position: absolute; z-index: 2;</code> и начальные <code>top</code>/<code>left</code>.</li>
</ul>
</li>
<li><strong>JavaScript-функция (анимация):</strong>
<ul>
<li>Определить размеры окна <code>window.innerWidth</code>, <code>window.innerHeight</code>.</li>
<li>Получить размеры изображений.</li>
<li>Использовать переменные для текущей позиции (<code>x</code>, <code>y</code>) и направления движения (<code>directionX</code>, <code>directionY</code>).</li>
<li>В функции, вызываемой <code>setTimeout</code>:
<ul>
<li>Изменять <code>x</code> и <code>y</code> в зависимости от <code>directionX</code> и <code>directionY</code>.</li>
<li>Обновлять <code>style.left</code> и <code>style.top</code> анимированного изображения.</li>
<li>Проверять границы (правая, левая, верхняя, нижняя) и менять <code>directionX</code>/<code>directionY</code> при достижении границы.</li>
<li>Вызывать <code>setTimeout</code> снова для следующего кадра анимации.</li>
</ul>
</li>
</ul>
</li>
</ol>
<p><strong>Примерный JavaScript-код и CSS:</strong></p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span>Лаб. работа 4 - Задание 3<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">
        <span class="token selector">body </span><span class="token punctuation">{</span> <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token property">overflow</span><span class="token punctuation">:</span> hidden<span class="token punctuation">;</span> <span class="token comment">/* Скрыть прокрутку, если есть */</span> <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#bg_image</span> </span><span class="token punctuation">{</span>
            <span class="token property">position</span><span class="token punctuation">:</span> absolute<span class="token punctuation">;</span>
            <span class="token property">top</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
            <span class="token property">left</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
            <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">50</span>vw<span class="token punctuation">;</span> <span class="token comment">/* 50% ширины viewport */</span>
            <span class="token property">height</span><span class="token punctuation">:</span> auto<span class="token punctuation">;</span>
            <span class="token property">z-index</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        <span class="token selector"><span class="token id">#moving_image</span> </span><span class="token punctuation">{</span>
            <span class="token property">position</span><span class="token punctuation">:</span> absolute<span class="token punctuation">;</span>
            <span class="token property">z-index</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>bg_image<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>p5_0.jpg<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Фон<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>moving_image<span class="token punctuation">"</span></span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>4.gif<span class="token punctuation">"</span></span> <span class="token attr-name">alt</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>Движущееся изображение<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>

    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>text/javascript<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
        <span class="token keyword">var</span> movingImage <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'moving_image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">var</span> bgImage <span class="token operator">=</span> document<span class="token punctuation">.</span><span class="token function">getElementById</span><span class="token punctuation">(</span><span class="token string">'bg_image'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

        <span class="token keyword">var</span> x <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Текущая x-координата</span>
        <span class="token keyword">var</span> y <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Текущая y-координата</span>
        <span class="token keyword">var</span> speed <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">;</span> <span class="token comment">// Скорость движения</span>
        <span class="token keyword">var</span> directionX <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// 1 = вправо, -1 = влево</span>
        <span class="token keyword">var</span> directionY <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// 1 = вниз, -1 = вверх, 0 = по горизонтали</span>

        <span class="token keyword">var</span> bgWidth<span class="token punctuation">,</span> bgHeight<span class="token punctuation">;</span>
        <span class="token keyword">var</span> movingImgWidth<span class="token punctuation">,</span> movingImgHeight<span class="token punctuation">;</span>

        <span class="token comment">// Инициализация размеров после загрузки изображений</span>
        window<span class="token punctuation">.</span><span class="token function-variable function">onload</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            bgWidth <span class="token operator">=</span> bgImage<span class="token punctuation">.</span>offsetWidth<span class="token punctuation">;</span>
            bgHeight <span class="token operator">=</span> bgImage<span class="token punctuation">.</span>offsetHeight<span class="token punctuation">;</span> <span class="token comment">// Может быть не совсем точо, если auto.</span>

            movingImgWidth <span class="token operator">=</span> movingImage<span class="token punctuation">.</span>offsetWidth<span class="token punctuation">;</span>
            movingImgHeight <span class="token operator">=</span> movingImage<span class="token punctuation">.</span>offsetHeight<span class="token punctuation">;</span>

            <span class="token comment">// Начальные координаты</span>
            movingImage<span class="token punctuation">.</span>style<span class="token punctuation">.</span>left <span class="token operator">=</span> x <span class="token operator">+</span> <span class="token string">'px'</span><span class="token punctuation">;</span>
            movingImage<span class="token punctuation">.</span>style<span class="token punctuation">.</span>top <span class="token operator">=</span> y <span class="token operator">+</span> <span class="token string">'px'</span><span class="token punctuation">;</span>

            <span class="token function">animate</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Запуск анимации</span>
        <span class="token punctuation">}</span><span class="token punctuation">;</span>

        <span class="token keyword">function</span> <span class="token function">animate</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token comment">// Движение по горизонтали до правой границы</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>directionY <span class="token operator">===</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                x <span class="token operator">+=</span> speed <span class="token operator">*</span> directionX<span class="token punctuation">;</span>
                <span class="token keyword">if</span> <span class="token punctuation">(</span>x <span class="token operator">+</span> movingImgWidth <span class="token operator">&gt;=</span> bgWidth<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    x <span class="token operator">=</span> bgWidth <span class="token operator">-</span> movingImgWidth<span class="token punctuation">;</span> <span class="token comment">// Установить точно на границе</span>
                    directionX <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Остановить горизонтальное движение</span>
                    directionY <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Начать движение вниз</span>
                <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>x <span class="token operator">&lt;=</span> <span class="token number">0</span> <span class="token operator">&amp;&amp;</span> directionX <span class="token operator">===</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Если движемся влево и достигли левой границы</span>
                    x <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
                    directionX <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
                    directionY <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Начать движение вниз</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>directionX <span class="token operator">===</span> <span class="token number">0</span> <span class="token operator">&amp;&amp;</span> directionY <span class="token operator">===</span> <span class="token number">1</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Движение вниз</span>
                y <span class="token operator">+=</span> speed<span class="token punctuation">;</span>
                <span class="token keyword">if</span> <span class="token punctuation">(</span>y <span class="token operator">+</span> movingImgHeight <span class="token operator">&gt;=</span> bgHeight <span class="token operator">&amp;&amp;</span> x <span class="token operator">+</span> movingImgWidth <span class="token operator">&gt;=</span> bgWidth<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Заканчиваем вниз, начинаем влево-вверх</span>
                    y <span class="token operator">=</span> bgHeight <span class="token operator">-</span> movingImgHeight<span class="token punctuation">;</span>
                    directionY <span class="token operator">=</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Движение вверх</span>
                    directionX <span class="token operator">=</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Движение влево</span>
                <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>y <span class="token operator">+</span> movingImgHeight <span class="token operator">&gt;=</span> bgHeight <span class="token operator">&amp;&amp;</span> x <span class="token operator">===</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Заканчиваем вниз</span>
                    y <span class="token operator">=</span> bgHeight <span class="token operator">-</span> movingImgHeight<span class="token punctuation">;</span>
                    directionY <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
                    directionX <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Теперь двигаемся вправо</span>
                <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>y <span class="token operator">+</span> movingImgHeight <span class="token operator">&gt;=</span> bgHeight<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Движение вниз до границы</span>
                    y <span class="token operator">=</span> bgHeight <span class="token operator">-</span> movingImgHeight<span class="token punctuation">;</span>
                    <span class="token comment">// Если дошли до низа, но не до конца по X</span>
                     directionY <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Остановить вертикальное движение</span>
                     directionX <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Начать движение вправо (снова)</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>directionY <span class="token operator">===</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token comment">// Движение вверх-влево</span>
                x <span class="token operator">+=</span> speed <span class="token operator">*</span> directionX<span class="token punctuation">;</span>
                y <span class="token operator">+=</span> speed <span class="token operator">*</span> directionY<span class="token punctuation">;</span>
                <span class="token keyword">if</span> <span class="token punctuation">(</span>x <span class="token operator">&lt;=</span> <span class="token number">0</span> <span class="token operator">&amp;&amp;</span> y <span class="token operator">&lt;=</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    x <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
                    y <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
                    directionX <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span> <span class="token comment">// Начать движение вправо</span>
                    directionY <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> <span class="token comment">// Остановить вертикальное движение</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">}</span>


            movingImage<span class="token punctuation">.</span>style<span class="token punctuation">.</span>left <span class="token operator">=</span> x <span class="token operator">+</span> <span class="token string">'px'</span><span class="token punctuation">;</span>
            movingImage<span class="token punctuation">.</span>style<span class="token punctuation">.</span>top <span class="token operator">=</span> y <span class="token operator">+</span> <span class="token string">'px'</span><span class="token punctuation">;</span>

            <span class="token comment">// Рекурсивный вызов для следующего кадра</span>
            <span class="token function">setTimeout</span><span class="token punctuation">(</span>animate<span class="token punctuation">,</span> <span class="token number">20</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 20 мс для более плавной анимации</span>
        <span class="token punctuation">}</span>
    </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>

<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p>Это сложная анимация, и предложенный выше код — это одна из возможных реализаций. Возможно, потребуется подгонка логики <code>if-else</code> для идеального соответствия описанию движения. При необходимости, можно упростить движение до простых циклов по четырем углам.</p>
<hr>
<p>К сожалению, я не могу физически <code>выполнить</code> лабораторные работы, как это делает человек в браузере или IDE. Но я предоставил вам пошаговые объяснения и примеры кода для каждого из запрошенных заданий, которые вы можете использовать для самостоятельного выполнения.</p>

