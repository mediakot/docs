###Виджет для плагина ManagerManager, предназначен для выбора id определённых документов в удобном виде

mm_ddSelectDocuments($tvs, $roles, $templates, $parentIds, $depth, $filter, $max, $labelMask);

####Описание параметров
Название|Описание|Допустимые значения|Значение по умолчанию|Обязателен?
--------|--------|---------|--------|--------
tvs|Имена TV, для которых необходимо применить виджет.|{comma separated string}|—|true
roles|Роли, для которых необходимо применить виждет, пустое значение — все роли.|{comma separated string}|—|false
templates|Id шаблонов, для которых необходимо применить виджет, пустое значение — все шаблоны.|{comma separated string}|—|false
parentIds|Id родительских документов, дочерние документы которых необходимо выбирать.|{comma separated string}|—|true
depth|Глубина поиска дочерних документов.|{integer}|1|false
filter|Условия фильтрации документов (чем-то похож на фильтр Ditto), разделённые через '&' между парами и через '=' между ключом и значением. Например: 'template=15&published=1', — получим только опубликованные документы с id шаблона 15.|{separated string}|—|false
max|Максимальное количество документов, которое пользователь может выбрать (при == 0 — без ограничений).|{integer}|0|false
labelMask|Шаблон отображения элемента в списке выбора документов. Задаётся как строка, содержащая плэйсхолдеры с полями документа (и TV). Также доступен дополнительный плэйсхолдер '[+title+]', в который будет подставлено значение поля «menutitle», а если оно не заполнено, то «pagetitle».|{string}|'[+title+] \([+id+]\)'|	false