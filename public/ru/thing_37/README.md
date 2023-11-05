# Не игнорируйте ошибки.
(В оригинале - Don't Ignore that Error!)

> *Однажды вечером я шел по улице на встречу с друзьями в баре. Мы уже давно не встречались попить пива, поэтому я спешил на встречу. И в спешке я не смотрел под ноги. А зря. Тогда бы я вовремя заметил бордюрный камень, так некстати подвернувшийся мне под ногу.*

> *Споткнувшись, я, похоже, повредил ногу, но я же спешил на встречу! Я продолжил свой путь несмотря на то, что боль все усиливалась. Поначалу я ее почти не замечал, но по мере того, как боль нарастала, я начал подозревать, что с ногой что-то не так.*

> *Но ведь я же спешил на встречу с друзьями! И когда я добрался до бара, боль стала невыносимой. Я не получил никакого удовольствия из-за боли. А когда утром я пошел к врачу, оказалось, что у меня сложный перелом голени. Остановись я сразу, как только почувствовал боль, проблем было бы гораздо меньше – ходьба на сломанной ноге ни к чему хорошему не приводит. Возможно, это было худшим утром в моей жизни.*


Слишком много программистов пишет столь же неосмотрительно, как вел себя я той ночью.

*Ошибка? Какая еще ошибка? Она наверняка несерьезная. Честно. Я могу не обращать на нее внимания.* Однако это проигрышная стратегия. А если честно, это всего лишь лень (причем лень неконструктивная!). Какой бы ничтожной ни была на ваш взгляд ошибка в вашем коде, она обязательно должна быть исправлена или обработана. Всегда. Вы не выиграете время, если не сделаете этого. Вы лишь спрячете потенциальную проблему на будущее.

Мы оповещаем об ошибках во время выполнения различными способами:
- **Код возврата**. Он может применяться для оповещения о том, что «что-то пошло не так». Код возврата слишком просто проигнорировать. И вы ничего не заметите вообще. Более того, игнорирование кодов возврата некоторых стандартных функций стало уже традицией. Как часто вы проверяете код возврата функции printf()?
- **errno**. Это такая особенность С, глобальная переменная, хранящая код последней случившейся ошибки. Его легко проигнорировать, сложно использовать, к тому же его использование вызывает множество других проблем – представьте многопоточную систему, в которой вызывается одна и та же функция. Некоторые платформы что-то делают, чтобы облегчить использование errno, другие не делают ничего.
- **Исключения**. Более структурированная языковая конструкция для сообщения об ошибках. К тому же, вы не можете их игнорировать. Или все же можете? Как насчет вот такого кода?

```
try {
    // ...do something...
}
catch (...) {} // ignore errors
```

Единственное оправдание этой ужасной конструкции – это то, что она явно показывает то, что вы делаете очень нехорошую вещь.

Если вы игнорируете ошибку в надежде, что ничего не случится, вы сильно рискуете. Как моя нога, пострадавшая гораздо сильнее, чем могла бы, если бы я тогда вовремя остановился. Если вы двигаетесь вперед без оглядки, вы можете столкнуться с очень серьезными проблемами. Решайте проблемы как можно раньше после их возникновения!

Игнорирование ошибок приводит к:
- **Ненадежному коду**. Коду, наполненному неуловимыми и сложноисправляемыми ошибками.
- **Небезопасному коду**. Хакеры часто используют игнорирование кодов ошибок, и очень часто делают это весьма успешно, «ломая» системы.
- **Плохо структурированному коду**. Если аккуратная обработка ошибок слишком скучна, скорее всего, это результат плохо продуманного интерфейса. Переделайте его так, чтобы обрабатывать ошибки было не так обременительно.


Кроме проверки всех потенциальных ошибок, нужно еще делать видимыми все потенциально возможные ошибочные состояния ваших интерфейсов. Не скрывайте их, расчитывая на то, что это будет работать.

- Почему мы не проверяем ошибки? Есть несколько общепринятых отговорок. С какими из них вы согласитесь?
Обработка ошибок загромождает код, делая его нечитаемым и не позволяя легко отследить основной поток выполнения.
- Обработка ошибок требует дополнительных усилий, а у меня дедлайн надвигается.
- Я уверен, что эта функция никогда не вернет ошибку (printf работает всегда, malloc всегда выделит запрашиваемый объем памяти, а если нет – мы все равно ничего не сможем сделать, ведь это значит, что не работает вся система)
- Это несерьезная программа, нет смысла ее писать с промышленным качеством.


Автор оригинала - [Pete Goodliffe](http://programmer.97things.oreilly.com/wiki/index.php/Pete_Goodliffe)