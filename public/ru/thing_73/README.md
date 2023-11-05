# Простота от уменьшения
(В оригинале - Simplicity Comes from Reduction)

«Переделай это…» - сказал мой босс, нажимая и держа клавишу Delete. Я смотрел на экран со знакомым многим чувством позора, пока мой код строка за строкой отправлялся в небытие.

Мой босс не отличался красноречивостью, однако он определял плохой код с первого взгляда. И он точно знал, что с таким кодом надо делать.

Я пришел на свою нынешнюю должность студентом с кучей энергии и энтузиазма, но вообще без идей о том, как же нужно писать код. Тогда мне казалось, что любую проблему можно решить, добавив куда-нибудь еще одну переменную или дописав еще одну строку кода. И однажды вместо того, чтобы улучшаться с каждой новой версией, мой код стал громоздким, сложным и далеким от целостности.

Это естественно, что в состоянии спешки вы хотите менять код как можно меньше, даже если это минимальное изменение и окажется просто ужасным. Большинство программистов оставят плохой код, опасаясь, что его переписывание займет слишком много времени. Это может сработать для кода, очень близкого к рабочему состоянию. Но бывает код, которому уже ничего не поможет.

Для спасения плохого кода может потребоваться слишком много времени. Как только что-то становится пожирателем ресурсов, это должно быть отброшено. Быстро.

Нет, конечно, необязательно выбрасывать все написанное. Реакция моего босса была крайностью, но при этом она заставила меня хорошо подумать над следующей версией. Однако, лучшим вариантом для исправления плохого кода все равно будет безжалостный рефакторинг и удаление.

Код должен быть простым. В нем должно быть как можно меньше переменных, функций, объявлений и других языковых конструкций. Лишние строки, лишние переменные, лишнее что угодно должно быть подчищено. Удалено. То, что останется, должно быть минимумом, необходимым для того, чтобы код работал так, как запланировано. Все остальное – это только лишний шум, вносящий случайность и отвлекающий от главного потока. Скрывающий важные вещи.

И конечно же, если рефакторинг не помог, то просто удалите все и напишите его заново. Такое воссоздание с нуля часто помогает избавить код от значительной части лишнего мусора.

Автор оригинала - [Paul W. Homer](http://programmer.97things.oreilly.com/wiki/index.php/Paul_W._Homer)