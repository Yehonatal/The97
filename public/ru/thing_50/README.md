# Осторожнее с повторным использованием!
(В оригинале - Beware the Share)

Это был мой первый реальный проект. Я только что закончил университет и старался хорошо показать себя, задерживаясь по вечерам и разбираясь в написанном коде. Во время реализации своей первой функциональности я особо заботился, чтобы использовать все, чему я научился – комментирование, лог, помещение общего кода в библиотеки там, где это возможно. Однако ревью кода стало для меня грубым возвращением к реальности – повторное использование кода категорически не было одобрено.

Как же это было возможно? Ведь везде говорили, что повторное использование – одна из основных вещей профессиональной разработки! Все статьи, которые я читал, все книги, все профессионалы, обучавшие меня – все говорили именно так! Где же была ошибка?

Оказалось, я пропустил одну критическую вещь.

Контекст.

То, что в двух никак не связанных частях системы оказалась одинаковая логика, значило гораздо меньше, чем я думал. До того как я вынес эту общую логику во внешнюю библиотеку, эти две части никак друг от друга не зависели. Каждая часть могла меняться независимо от другой. В каждой части логика могла меняться при необходимости в зависимости от требования бизнес окружения. Эти строки одинакового кода не были ничем иным как простым совпадением. До тех пор, пока не пришел я.

Общая внешняя библиотека, которую я создал, связала обе части вместе. В результате уже нельзя было изменить одну часть без синхронизации изменения со второй частью. Если ранее стоимость сопровождения этих двух независимых функциональностей была незначительна, теперь, после появления общей библиотеки, необходимость тестирования значительно возросла.

Одновременно с уменьшением общего количества кода в системе я увеличил количество зависимостей в ней. Контекст этих зависимостей весьма важен – находись эти две функциональности рядом, такая зависимость могла бы быть оправдана. Однако когда функциональности вообще никак не связаны друг с другом, такая тесная зависимость становится проблемой, несмотря на то, что внешне код выглядит вполне нормально.

Эти ошибки коварны тем, что изначально выглядят как хорошие идеи и оптимизации. Будучи примененными в правильном контексте, эти техники могут принести пользу. В неправильном контексте их применение повысит лишь расходы, но не принесет пользы. И теперь, имея дело с написанным кодом без подробной информации о том, в каком контексте используются его отдельные части, я гораздо более осторожно отношусь к повторному использованию.

Будьте осторожны с повторным использованием. Сначала проанализируйте контекст, и только потом реализуйте.

Автор оригинала - [Udi Dahan](http://programmer.97things.oreilly.com/wiki/index.php/Udi_Dahan)