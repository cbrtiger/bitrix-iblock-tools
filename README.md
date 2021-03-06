Bitrix IBlock Tools
===================

Представляет класс CIBlockTools для CMS "1С-Битрикс", позволяющий без обращения к БД:

1.	Получить ID инфоблока по его коду (CODE),
2.	Получить ID свойства инфоблока по его коду (CODE),
3.	Получить ID значения свойства типа "список" по его XML_ID.

Класс хранит информацию о инфоблоках и их свойствах в кэше битрикса.
При любом изменении инфоблоков, свойств инфоблоков данный кэш автоматически обновляется.

Использование
-------------

Для использования достаточно подключить iblock_tools.php в /bitrix/php_interface/init.php

`````php
// Получение ID инфоблока по коду
$iblockId = CIBlockTools::GetIBlockId('код инфоблока');

// Получение ID свойства по коду инфоблока и коду свойства
$propertyId = CIBlockTools::GetPropertyId('код инфоблока', 'код свойства');

// Получение ID значение свойства типа "список"
// по коду инфоблока, коду свойства и XML_ID значения свойства
$propertyValueId = CIBlockTools::GetPropertyEnumValueId('код инфоблока', 'код свойства', 'XML_ID значения свойства');
`````