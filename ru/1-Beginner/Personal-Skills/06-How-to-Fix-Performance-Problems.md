# Как устранять проблемы производительности
[//]: # (Version:1.0.0)
Большинство проектов можно с относительно небольшими усилиями ускорить в 10-100 раз относительно их первой версии. В условиях сжатых сроков выхода на рынок разумно и эффективно выбирать ту реализацию, которая проще и быстрее остальных. Однако, производительность это часть удобства использования, поэтому часто ее стоит оценивать более внимательно.

Главное в улучшении производительности сложной системы - это проанализировать ее достаточно тщательно, чтобы найти "узкие места", то есть те места, где запрашивается наибольший объем ресурсов. Нет большого смысла оптимизировать функцию, которая занимает только 1% процессорного времени. Если вы не уверены, что изменение ускорит систему или ее значительную часть хотя бы в два раза, то стоит хорошо подумать, стоит ли это вообще делать. Как правило, такие способы ускорения есть. Оценивайте также затраты на тестирование и проверки, которые потребует ваше изменение кода. Каждое изменение кода влечет за собой необходимость тестирования, поэтому лучше иметь небольшое число значительных изменений.

После того, как вы добились двукратного улучшения производительности в одном месте, стоит снова проанализировать программу и определить следующее по затратам узкое место. Тогда можно заняться им.

Часто узкие места в производительности будут представлять собой что-то вроде подсчета коров по ногам и последующего деления на четыре вместо обычного подсчета по головам. Например, я часто забывал дать собственный индекс часто запрашиваемому столбцу в реляционной базе управления данных, что замедляло весь процесс минимум в 20 раз. Среди других примеров: ненужные операции чтения и записи в циклах, отладочные сообщения, ставшие неактуальными, избыточное выделение памяти и в особенности неумелое использование библиотек и сторонних фреймворков, которые плохо документированы в части производительности. Такой вид улучшений легко определить и с ходу внести в программу. 

Что делать, когда очевидных мест для улучшений не осталось? Вы можете продолжать искать узкие места на более глубоком уровне или пересмотреть весь дизайн системы. Последнее дает прекрасную возможность продемонстрировать свои умения программиста не только в реализации нового дизайна системы, но и в умении убедить своего босса в том, что это необходимо. Тем не менее перед тем, как вы начнете убеждать его в необходимости коренных изменений, спросите себя, ускорит ли ваше решение систему в 5-10 раз.

Следующее: [Как оптимизировать циклы](07-How-to-Optimize-Loops.md)
