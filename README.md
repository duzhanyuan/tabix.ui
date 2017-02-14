## Назначение
Данный проект представляет собой GUI для [OLAP Yandex Clickhouse](https://github.com/yandex/ClickHouse).

Последняя версия рабочего приложения: [master buid on github pages](http://guiclickhouse.smi2.ru/)

[Youtube demo](https://www.youtube.com/watch?v=u5DOWnm47vg)

![](https://raw.githubusercontent.com/smi2/clickhouse-frontend/master/media/screen4.jpg)
![](https://raw.githubusercontent.com/smi2/clickhouse-frontend/master/media/screen5.jpg)


## Требования 
* Версия сервера CH, старше  v1.1.54019-stable, process list >= 1.1.54159
* Пользователь с правами _не_ readonly 
* Разрешенный IP адресс



## Changelog 


### Dev ( > 2016-12-22  )
- [x]  Bind: Cmd-Y | Ctrl-Y = removeLines
- [x]  Автодополнение + подсказка по полям с типом 
- [x]  Автодополнение словарей + подсказка
- [x]  Возможность уменьшать редактор SQL
- [x]  Словари в автоподсказках "dic_*"
- [x]  Отображение числа таблиц у базы
- [x]  fix : Не показываются пустые базы
- [x]  Перестроение списка баз/таблиц после выволенения запроса DROP/CREATE
- [x]  Иконка таблицы зависит от Engine
- [x]  Подсказка при подключении в виде http://127.0.0.1:8123 , возможно использование httpS
- [x]  HTTP параметр,возможность устанавливать настройки для севера
- [x]  Список полей в таблице (левом дереве) и вставка поля при клике в редактор
- [x]  Запрос создания таблицы, через SHOW CREATE TABLE - в "информации" 
- [x]  Настройка автодополнение / enableLiveAutocompletion
- [x]  Размер div результата компактнее
- [x]  Подсветка скобок
- [x]  Список ф-ций загружатеся исходя из возможностей сервера. Из таблицы `system.functions` + keywordMapper.builtinFunctions
- [x]  Подсказка по функции (загрузка из json)
- [x]  [Command | Ctrl ] + [ Right | Left ] переключает вкладки
- [x]  Shift-Ctrl-[1...0] переключает вкладки 
- [x]  Редактор - иконки в подсказках
- [x]  Отдельное окно SHOW PROCESSLIST FORMAT JSON
- [x]  Подсказки из офф документации в виде Json/js 
- [x]  Редактор:Сворачивать скобки / Подзапросы
- [x]  Редактор:Выбор разделителя запросов `;;` или `;` 
- [x]  Комманда DRAW подсветка
- [x]  Отправка запросов post
- [x]  Сворачивать _все_ скобки 
- [x]  Переформатирование запросов/автоформат
- [x]  Контекстное меню у редактора, свернуть все/развернуть
- [x]  [Command|Ctrl+Shift+Plus | Command|Ctrl+Shift+Minus ] - свернуть все/развернуть
- [x]  [Command|Ctrl+Shift+F ] - Format code
- [x]  Виджет-ная стуктура (Плагинная структура для Renders)
- [x]  Виджеты через отрисовка gridster, резайз move, фиксация
- [x]  Моноширинная таблица результата и код ошибки, или текстовый ответ
- [x]  handsontable Таблица результата с сортировкой
- [x]  Автоподбор ширины таблицы результата
- [x]  TabiX name
- [X]  HotTable темная тема для меню и hottable в списке процессов
- [x]  PROCESSLIST режим логировать запросы
- [x]  HotTable ресайз колонок
- [x]  HotTable CopyPaste menu
- [x]  Menlo font
- [x]  В словарях поле ID строится из названия словаря, ads.blocks => block_id , ads.campaigns => campaign_id , ads.news => news_id , geonames => geoname_id
- [x]  SHOW PROCESSLIST не останавливается
- [x]  Меню по правой кнопке на таблице, наполнить элементы
- [x]  KILL QUERY WHERE в SHOW PROCESSLIST ("KILL QUERY WHERE query LIKE 'SELECT sleep(%' AND (elapsed >= 0.) SYNC"
- [x]  Меню для таблицы (по прав.кнопке )
- [x]  Улучшить отображение полей таблицы в дереве, поддержка клика , доп элементы у таблицы - меню по правому клику
- [x]  Редактор ACEjs,вынести из под Bower, ACE скрестить с Ace.Tern
- [x]  Live autocomplete delay
- [x]  KILL QUERY по query_id не по hash
- [x]  Выбор DB через двойной клик в дереве, вслывашка о выборе
- [x]  Дерево теперь не переключается
- [x]  HotTable ресайз виджета, и при инициализации не правильный размер
- [x]  Рендеры графики AmCharts + resize
- [x]  Рендеры графики eChars + resize
- [x]  echarts тема темная

**Todo high**:
- [ ] Редактор 
> - Парсинг в тексте FROM DBName.TBName,список доступных полей исходя из имени таблиц


- [ ] Переменные
> - Парсинг в тексте "Переменные" и их подсветка
> - Подстановка в запросах $vars переменных
> - Таблица редактор $vars


- [ ] Рендер
> - Рендеры графики angular-nvd3
> - Рендер стандартной таблицы с фильтрами + сортировка ( клиенте/  сервером ) Grid

- [ ]  AmCharts тема темная, color
- [ ]  Поиск в дереве обьектов, фильтрация дерева


- [ ]  HotTable запоминать размеры установленные руками ( не сбрасывать в ноль )
- [ ]  HotTable в сплывашке показывается криво
- [ ]  HotTable CopyPaste to ReadMine markup
- [ ]  Export/import Widgets,DrawWidgets
- [ ]  PivotJS не работает Drag&Drop
- [ ]  Переиминовать в коде CHGui в Tabix
- [ ]  Поправить верстку шапки
- [ ]  DRAWSET, реализовать парсер, задает параметры области рендера результата
- [ ]  Размер несжатых данных
- [ ]  Позиция ошибки в корявом sql, парсить ошибку на строку + позицию , заставить Ace найти этот запрос и отпозиционироваться Syntax error: failed at position 25 (line 2, col 4)
- [ ]  Виджет список предустановленных графиков + минимальный редактор


- [ ]  Документация
> - Help Modal Window -> Link to github +  Hotkey справочник и/или help
> - Отдельный домен doc.tabix, собранный из md файлов , Live Docs by dgeni https://github.com/angular/dgeni


**Todo low**:
- [ ] tableau export via WDC/ODATA
- [ ] Ошибка ``Не введен SQL``
- [ ] Ошибка позиции `;;\n
                      select 2\n
                      ;;<cursor>\n
                      select 4\n` в коде `item.range.compare(cursor.row, cursor.column) !== 0)`
 


----
*Построение графи.*
sankeys in Tableau: https://community.tableau.com/thread/154623

http://echarts.baidu.com/demo.html#sankey-product

http://echarts.baidu.com/demo.html#treemap-drill-down

http://echarts.baidu.com/examples.html

https://cdn.materialdesignicons.com/1.1.34/

**ACE**
http://krispo.github.io/angular-nvd3/#/

https://github.com/ajaxorg/ace/wiki/Configuring-Ace

https://github.com/tlatoza/SeeCodeRun/wiki/Ace-code-editor

https://masonwebdev.wordpress.com/2016/03/22/extending-ace-lets-make-sure-you-are-always-with-higher-hand/

----
material design icons : https://cdn.materialdesignicons.com/1.1.34/
----
tableau: 

https://community.tableau.com/community/developers/web-data-connectors
https://github.com/justindarc/fxos-web-server
https://onlinehelp.tableau.com/current/server/en-us/datasource_wdc.htm
https://github.com/wangshijun/angular-echarts

----

**awesome-dataviz**

https://github.com/fasouto/awesome-dataviz


http://raw.densitydesign.org/



# Draw 

### drawchart

```javascript
{
    cos:{'lineColor':'green','type':'column'},
    sin:{'title':'COS!!!!'}
}
```
### drawsankeys

```javascript
{
    levels:[
        {source:'AdmArea',target:'District',value:'MoneyPerHour'},
        {source:'District',target:'Street',value:'MoneyPerHour'}
    ],
    echarts:{}
}
```

----

### 2016-12-17

* "Order by и group by" - подсветка fix
* Разделитель запросов 


### 2016-12-11

* Добавлена поддержка английского языка. Язык выбирается автоматически в зависимости от настроек браузера
* httpS поддержка - если указать в подключении https://ip:port 

### 2016-11-03
Полностью обновили GUI 
Вместо слов : https://monosnap.com/file/rIEnBkDoh0jMmhGDsu0umaqk5F0srt 


### 2016-10-12
* Запрос на create_table из select , если запрос содержит таблицу ответа 
* Сортировка словарей по name + удобное отображение
* Выполнение запроса "под курсором"  
* Shift-Ctrl-Enter | Shift-Command-Enter - запустить все запросы разделенные ;; или выделенный 
* Ctrl-Enter | Command-Enter - запускает текущий или выделенный 
* Размер таблицы 
* Исправлена загрузка шрифтов. 
* Вынесен screenfull из html в зависимости
* Изменения в шаблоне lumX

### 2016-10-11
* Показ версии сборки
* Автодополнение, поддержка словарей - отдельная кнопка вставить словать
* Прогресс бар запросов
* Правки подсветки IF EXISTS + IF NOT EXISTS
* Отрисовка ответа после create/drop/insert + обновление автодополнения

### 2016-10-10
* Добавили поддержку FORMAT CSV|FORMAT CSVWithNames в запросе + подсветка + дополнение
* В редакторе добавленна возможность максимальное кол-во строк в ответа
* Развернуть в полный экран редактор запросов 
* HotKey ⌘ + ⏎ для мак , выполнить запрос или выполнить выделенный запрос только 
* История запросов, показывает последний успешный запрос при открытии GUI 
* Анонимное подключение к базе без указания user+password  
* Корректная подсветка и автодополние, теперь автодополнение содержит колонки и названия таблиц
* Последовательное выполнение нескольких запросов которые разделены `;;`



Пример тестового запроса: 
```sql

;;select 0 as ping;;
select 1 as ping;;select 2 as ping
;;select 3+sleep(0.1) as ping;;select 4+sleep(0.1) as ping;;
SELECT 5 As PING format JSON;;select 6 as ping
;;select 7 as ping FORMAT CSVWithNames
;;CREATE TABLE IF NOT EXISTS t (a UInt8,b String) ENGINE = Log;;
INSERT INTO t SELECT toUInt8(123) as a,';;' as b  
;;DROP TABLE IF EXISTS t;;DROP DATABASE IF EXISTS xzxz;;

```


# Dev

## Зависимости
Необходимо установить
* NodeJS >= 5.x. ( лучше v6.7.0 )

Установить глобальные NPM пакеты Gulp и Bower, загрузить зависимости:
<pre>
sudo npm install bower -g
sudo npm install gulp -g
npm install
bower install
</pre>

## Сборка
Для разработки:
<pre>
gulp serve
</pre>
На production:
<pre>
gulp build
</pre>

Для сборки документации:
<pre>
gulp docs
</pre>
