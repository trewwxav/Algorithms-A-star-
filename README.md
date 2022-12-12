# A star algorithm


| info          |               |
| ------------- | ------------- |
| ВУЗ | ДВФУ|
| Направление   | Б9121-09.03.03пикд|
| ФИО      | Шкарина Дарья Евгеньевна|

____

# Cодержание <a name="Cодержание"></a>

- [Содержание](#Cодержание)
- [Глоссарий](#Глоссарий)
- [Постановка задачи](#Постановказадачи)
- [Введение](#Введение)
- [Использование](#Использование) 
	-  [Основная концепция и описание работы алгоритма](#Основнаяконцепцияиописаниеработыалгоритма)
- [Список литературы](#Списоклитературы)

# Глоссарий <a name="Глоссарий"></a>

1. `Алгоритм Дейкстры` это алгоритм на графах, изобретённый нидерландским учёным Эдсгером Дейкстрой в 1959 году. находит кратчайшие пути от заданной вершины  до всех остальных в графе без ребер отрицательного веса. 
2. `Эвристическая функция` это функция, которая не выведена математически строго, а придумана на основании каких-то соображений.
3. `Взвешенный граф` это граф, в котором у каждого ребра и/или каждой вершины есть “вес” - некоторое число, которое может обозначать длину пути, его стоимость и т. п.



# Постановка задачи <a name="Постановказадачи"></a>

Изучить, описать и реализовать алгоритм A*

# Введение <a name="Введение"></a>

 _A star ( A*) алгоритм_ -  алгоритм поиска по первому наилучшему совпадению на графе, который находит маршрут с наименьшей стоимостью от начальной вершины к целевой.

![AStar](https://user-images.githubusercontent.com/98378287/206121400-d5dc0ce7-b0b8-49c0-b222-14683123e79f.gif)

 
Алгоритм А* — один из самых эффективных алгоритмов поиска кратчайшего пути между двумя точками графа. Он был опубликован Питером Хартом, Нильсом Нильссоном и Бертрамом Рафаэлем в 1968 году. В каком-то смысле его можно назвать расширением алгоритма Дейкстры. Однако, несмотря на это он является одним из самых часто используемых алгоритмов поиска пути.

Основная разница между Алгоритмом Дейкстры и A* заключается в том что алгоритм Дейкстры находит кратчайшие пути для всех точек на графе, в то время как А* оптимизирован для нахождения кратчайшего пути до одной точки, что позволяет существенно сократить время работы алгоритма.

алгоритм А* находит оптимальный вариант благодаря вычислению суммарной стоимости всех путей между начальной и конечной точкой. Этот способ считается быстрее алгоритма Дейкстры благодаря эвристической функции.

Алгоритм А* обладает двумя ключевыми характеристиками алгоритмов такого рода: **оптимальность** и **полнота**.

> Если алгоритм поиска характеризуется как **оптимальный**, значит он гарантирует получение **лучшего из возможных решений**. А когда среди характеристик присутствует определение **«полный»**, это означает, что алгоритм **всегда находит** решение, если таковое **существует**.

A* пошагово просматривает все пути, ведущие от начальной вершины в конечную, пока не найдёт минимальный.

____

# Использование <a name="Использование"></a>

**A*** — это модификация алгоритма Дейкстры, оптимизированная для единственной конечной точки. Алгоритм Дейкстры может находить пути ко всем точкам, A* находит путь к одной точке. Он отдаёт приоритет путям, которые ведут ближе к цели.

А* идеально подходит для любой задачи где нужно найти кратчайшее расстояние к конечной точке, и из-за этого алгоритм оказался очень хорошо заточен для компьютерных игр, где часто используется.

Еще один аспект, делающий A* таким мощным, — это использование в его реализации взвешенных графов. Взвешенный граф использует числа для представления стоимости каждого пути или курса действий. Это означает, что алгоритмы могут выбрать путь с наименьшими затратами и найти лучший маршрут с точки зрения расстояния и времени.

![graph](https://user-images.githubusercontent.com/98378287/206944296-612905dd-c56a-40d2-bdc4-a1860b5611d6.png)



## Основная концепция и описание работы алгоритма <a name="Основнаяконцепцияиописаниеработыалгоритма"></a>

Эвристический алгоритм жертвует оптимальностью, точностью и аккуратностью ради скорости, чтобы решать проблемы быстрее и эффективнее.

Все графы имеют разные узлы или точки, которые должен пройти алгоритм, чтобы достичь конечного узла. Все пути между этими узлами имеют числовое значение, которое считается весом пути. Сумма всех поперечных путей дает вам стоимость этого маршрута.

Первоначально алгоритм вычисляет стоимость для всех своих ближайших соседних узлов, n, и выбирает тот, который несет наименьшую стоимость. Этот процесс повторяется до тех пор, пока не будут выбраны новые узлы и не будут пройдены все пути. Затем вы должны рассмотреть лучший путь среди них. Если f(n) представляет окончательную стоимость, то ее можно обозначить как:

$$f(n) = g(n) + h(n),$$ где: $$g(n) =$$ стоимость перехода от одного узла к другому. Это будет варьироваться от узла к узлу $$h(n) =$$ эвристическая аппроксимация значения узла. 


Стоимость перехода от одной клетки к другой определяется несколькими значениями. 

\\используем либо расстояние чебышева либо манхэттенское для вычисления веса переода от одной клетки к другой\\

____

# Список литературы <a name="Списоклитературы"></a>

1. https://en.wikipedia.org/wiki/A*_search_algorithm
2. https://towardsdatascience.com/a-star-a-search-algorithm-eb495fb156bb
3. https://www.simplilearn.com/tutorials/artificial-intelligence-tutorial/a-star-algorithm#algorithm
4. https://www.geeksforgeeks.org/a-search-algorithm/
