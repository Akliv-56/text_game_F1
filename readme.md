# Проект: Artem and Animals...

### Суть проекта

1. У нас есть 5 этажей
2. На каждом этаже ровно 5 комнат
3. Всего в игре 30 комнат

### Комната

1. Может иметь: МОНСТР, ЛУТ-БОКС, БОС


### Монстры
1. **Бывают двух видов**: Melee, Range
2. **Характиристики**: Название, Жизни, Сила Атаки
3. У всех моснтров есть три уровня. 1- когда атака монстра больше N, 2-когда больше K, и 3-когда больше J.

#### Melee монстр
1. Атака - обычная
2. Урон получает обычным способом

#### Range монстр
1. Атака - обычная
2. Урон получает обычным способом. Есть 30% шанс, что игрок совершит промах.

### Лут-Боксы
1. Любой лут-бокс, должен дать сразу 4 на выбор предмета.
2. Предметы: Оружие, Броня, Расходники.

# Docs API

## Agents

### Player

##### Описание

##### Данная функция создает агента принимая на вход два массива int

```Python
def create_players(name:str, health:int,bonus_health:int,damage:int,bonus_damage:int) -> list:[str,int,int,int,int]:
    pass
```
в результате исполнения возвращает массив состоящий из пяти эллементов

- str - имя пользователя
- int - количество жизней
- int - количество бонусных жизней
- int - количество урона
- int - количетсво бонусного урона

### Melee

##### Описание
Данная функция создает агента ближнего боя, рандомно конфигурирует его: наименование, уровень, здоровье и урон.

##### Функция

```Python
def create_monster() -> list[str, int, int, int]: 
    pass
```
в результате исполнения, возвращает монстра в формате массива из четырех элементов.
- str - наименование монстра
- int - уровень
- int - здоровье
- int - наносимый урон

### Ranged

##### Описание
Данная функция создает агента дальнего боя, рандомно конфигурирует его: наименование,уровень,здоровье и урон.

##### Функция

```Python
def create_ranged_monster() -> list[str,int,int,int]:
    pass
```
в результате исполнения, возвращает монстра в формате массива четырех элементов.
- str - наименование монстра
- int - уровень
- int - здоровье
- int - наносимый урон
