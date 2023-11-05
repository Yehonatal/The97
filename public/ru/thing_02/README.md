# Будьте предусмотрительны
(В оригинале Act with Prudence)

> *«Чем бы вы не занимались, делайте это с предусмотрительностью и думайте о результатах»* - автор неизвестен.

Каким бы легким не выглядело расписание в начале итерации, вам не избежать того, что иногда придется работать под давлением. Если вам приходится выбирать между «сделать хорошо» и «сделать быстро», то часто выбор падает на «сделать быстро» сейчас, а потом доделать как надо. Когда вы даете такое обещание себе, команде и заказчику, вы действительно в это верите. Но потом следующая итерация приносит свои проблемы, и вам приходится решать их. Для такой отложенной работы появился неологизм «технический долг» ([technical debt](http://martinfowler.com/bliki/TechnicalDebtQuadrant.html)). Говоря еще точнее, Martin Fowler называет его «преднамеренный технический долг», в противоположность «непреднамеренному».

У технического долга много общего с долгом обычным. Вначале вы получаете кратковременную выгоду, но потом вам приходится платить проценты до полной выплаты долга. «Срезание углов» в коде затрудняет дальнейшую модификацию или рефакторинг. Такой код становится рассадником ошибок и ненадежных тестовых сценариев. Чем дольше вы его оставляете без изменений, тем хуже он становится. К тому времени как вы соберетесь наконец-то все исправить, окажется, что уже из-за той самой неисправленной ошибки на проекте несколько раз было принято не самое лучшее решение, и из-за этих новых надстроек исправление не так просто сделать. И часто единственное, что реально вынудит вас таки вернуться и сделать исправление – положение из серии «хуже уже некуда». При этом исправление возможно станет столь сложным, что потребует слишком много времени или окажется слишком рискованным.

Иногда действительно приходится «повесить» на себя технический долг для того, чтобы успеть к дедлайну или реализовать требуемую функциональность. Старайтесь не попадать в такую ситуацию, но если вдруг избежать ее не получится, тогда просто сделайте это. Но! Обязательно отслеживайте технических долг и старайтесь оплатить его быстро, иначе проблемы начнут расти как снежный ком. Как только вы пошли на компромисс, внесите исправление этого в систему трекинга задач, чтобы не забыть о нем.

Если вы запланируете исправление долга в следующей итерации, потери будут минимальными. Оставление долга неоплаченным вызовет накопление процентов, и эти проценты тоже должны отслеживаться, чтобы визуализировать затраты. Это подчеркнет эффект технического долга на проекте и позволит правильно расставить приоритеты. То, как именно подсчитывать и отслеживать «проценты» по техническому долгу, зависит от конкретного проекта, но делать этот учет вы обязаны.

Оплачивайте технический долг как можно быстрее. Действовать по-другому было бы неосмотрительно.

Автор оригинала - [Seb Rose](http://programmer.97things.oreilly.com/wiki/index.php/Seb_Rose)