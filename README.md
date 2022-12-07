# A star algorithm


| info          |               |
| ------------- | ------------- |
| ВУЗ | ДВФУ|
| Направление   | Б9121-09.03.03пикд|
| ФИО      | Шкарина Дарья Евгеньевна|


# Cодержание

# Постановка задачи


# Введение

 ## _A star ( A*) алгоритм_ -  алгоритм поиска по первому наилучшему совпадению на графе, который находит маршрут с наименьшей стоимостью от начальной вершины к целевой.
 
Алгоритм А* — один из самых эффективных алгоритмов поиска кратчайшего пути между двумя точками графа. Он был опубликован Питером Хартом, Нильсом Нильссоном и Бертрамом Рафаэлем в 1968 году. В каком-то смысле его можно назвать расширением алгоритма Дейкстры. Однако, несмотря на это он является одним из самых часто используемых алгоритмов поиска пути.

алгоритм А* находит оптимальный вариант благодаря вычислению суммарной стоимости всех путей между начальной и конечной точкой. Этот способ считается быстрее алгоритма Дейкстры благодаря эвристической функции.

Алгоритм А* обладает двумя ключевыми характеристиками алгоритмов такого рода: **оптимальность** и **полнота**.

> Если алгоритм поиска характеризуется как **оптимальный**, значит он гарантирует получение **лучшего из возможных решений**. А когда среди характеристик присутствует определение **«полный»**, это означает, что алгоритм **всегда находит** решение, если таковое **существует**.

A* пошагово просматривает все пути, ведущие от начальной вершины в конечную, пока не найдёт минимальный.

# Использование

**A**** — это модификация алгоритма Дейкстры, оптимизированная для единственной конечной точки. Алгоритм Дейкстры может находить пути ко всем точкам, A* находит путь к одной точке. Он отдаёт приоритет путям, которые ведут ближе к цели.

. А* идеально подходит для любой задачи где нужно найти кратчайшее расстояние к конечной точке, и из-за этого алгоритм оказался очень хорошо заточен для компьютерных игр, где часто используется.

