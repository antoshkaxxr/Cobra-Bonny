## Ревью
 
Игра интересная, не играл в змейки со времён nokia 3310 ))
Но в отличие от оригинала здесь имеется множество припятствий и усложнений получения заветных
очков. Единственное, что мне показалось интуитивно непонятно: в самый первый раз я не заметил очки в виде точек 
на карте и потому направился в одну из комнат к смайлу - так я не успел опомниться как проиграл.

### Коментарии по классам:

#### Main
- Всё чётко, ничего лишнего

#### CobraGame
- В целом интуитивно понятный класс, где ,как мне кажется, каждое действие оправдано

#### CobraGrid
- Касаемо метода placePoint: очень здорово что point может появиться только там куда доберётся змейка.
Однако может смущать то, что в методе if на каждый объект написан
- Немного странно, все начальные объекты отрисоввываются в сущности связанной с управление кобры (PS не знаю корректно ли в JAck делать претензии к ООП)
- В методе initGrid много вещей который можно сделать как функции непринимающих аргументы(например отрисовка теннисных столов)

#### Cobra
- Хотелось бы, чтобы проверка на то, что находится движущийся объект (змейка или точка) на каком-то объекте карты, в одной функции. Как мне кажется коды в CobraGrid в методе checkOccupied и в Cobra в методе tryMove можно попробовать упростить и объеденить. НО: на мой взгляд, это будет неопарданно с точки зрения затраты сил и времени, ведь в движениях кобры нужно под каждый вид движения написать свои условия.

#### Random
- В методе rand прикольно сделано получение положительного числа при помощи вычитания
- В randRange что-то сложное во что вникать не хочется но результат предельно ясен 
(PS больше всего смущает let ret = Random.rand() & mask; , где побитовое & с mask = 1)

#### RandomSeed
- Не очень понятна важность данной сущьности: содержащиеся в ней методы можно было оформиить в виде методов игры (а-ля подготовка к игре)
- Очень необычный способ получения рандомного числа

## Итог:
Игра очень классная, код продокументирован, в целом всё понятно как работает. Единственное для меня до сих пор не понятно, можно ли было избежать передачи CobraGame в CobraGrid и Cobra
