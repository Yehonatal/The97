# Много данных? Используйте СУБД!
(В оригинале - Large Interconnected Data Belongs to a Database)

Если ваше приложение работает с большим объемом связанных друг с другом данных, то без каких-либо сомнений помещайте их в реляционную базу данных. В прошлом реляционные базы данных (РДБ, или СУБД) были дорогими, редкими, сложными и громоздкими. Сейчас это не так. СУБД стали широко распространены (скорее всего, на вашем компьютере установлена одна или две). Среди них есть системы с открытым кодом, такие как MySQL и PostgreSQL, так что цена тоже перестала быть критическим фактором. И даже больше, СУБД реального времени могут линковаться в виде библиотек непосредственно в приложение, так что вам даже не придется иметь дело с процедурой установки. Среди СУБД реального времени можно выделить SQLite и HSQLDB. Эти системы обладают очень высокой эффективностью.

Если объем ваших данных превышает объем оперативной памяти, то индексированная таблица в БД будет в разы эффективнее, чем размещение данных в памяти с использованием механизма виртуальной памяти. Современные БД легко масштабируются по мере надобности. Соблюдая определенные правила, вы легко можете перейти от встраиваемой СУБД к более продвинутой, если это понадобится. Или перейти с бесплатной БД с открытым кодом к коммерческой, имеющей техподдержку и более масштабируемой.

Как только вы освоите SQL, написание БД-приложений станет для вас простым и приятным занятием. После внесения нормализованных данных в БД вы легко можете извлекать их в различных комбинациях и подмножествах при помощи понятных SQL-запросов. Простая SQL-команда легко может выполнить весьма сложное изменение данных. А для однократных изменений вам вообще не понадобится писать код, достаточно будет запустить SQL-интерфейс и ввести команду там. В этом же интерфейсе вы можете экспериментировать с различными запросами – вместо аналогичного цикла «редактирование-компиляция-запуск».

Еще одно преимущество использования СУБД – возможность задания отношений между элементами данных. Вы можете задать ограничения целостности данных и тем самым избежать риска получения «висящих указателей» в случае некорректной работы с данными. Например, вы можете указать, что при удалении пользователя необходимо удалить и все посланные им сообщения.

Кроме этого, вы всегда можете легко создать связи между данными в базе, используя индексы. Вам не потребуется делать дорогой и сложный рефакторинг полей классов. К тому же СУБД позволяет организовать безопасный доступ к данным множеству пользователей. Это дает вам возможность перейти при необходимости к многопользовательскому режиму, а также реализовывать различные части приложения на наиболее подходящих платформах и языках. Например, вы можете написать XML back-end для веб-приложения на Java, скрипт аудита на Ruby, а интерфейс визуализации – на [Processing](http://www.processing.org/).

И наконец, помните, что СУБД заботятся об оптимальном выполнении ваших SQL-команд, позволяя вам сконцентрироваться на функциональности приложения, а не на оптимизации алгоритмов. Продвинутые СУБД отлично работают на многоядерных процессорах. И по мере роста технологий будет расти и производительность вашего приложения.

Автор оригинала - [Diomidis Spinellis](http://programmer.97things.oreilly.com/wiki/index.php/Diomidis_Spinellis)