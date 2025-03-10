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

## Fight

### Fight melee

##### Описание
Данная функция принимает на вход агента игрока и агента ближнего монстра в ходе функции они забирают друг у друга здоровье 

##### Функция
```Python
def fight_monster_melee(player: list[str,int,int,int,int], monster: list[str, int,int, int]):
    pass
```
в результате исполнения выводит победителя и количество оставшихся жизней

### Fight ranged

##### Описание
Данная функция принимает на вход агента игрока и агента дальнего монстра в ходе функции они забирают друг у друга здоровье 

##### Функция
```Python
def fight_monster_ranged(player: list[str,int,int,int,int], ranged_monster: list[str, int,int, int]):
    pass
```
в результате исполнения выводит победителя и количество оставшихся жизней

## loot

### loot_box

##### Описание
Данная функция принимает на вход массивы с характеристиками предметов и рандомно выбирает однин из них

##### Функция
```Python
def loot_box(NAMES_ITEMS_DAMAGE,NAMES_ITEMS_HEALTH,ITEMS_DAMAGE,ITEMS_HEALTH,damage,skill,damage_list,health,health_list):
    pass
```
в результате выводит имя предмета и его характеристики

## character counter

### damage 

##### Описание
выводит урон в зависимости от выбора

##### Функция
```Python
def count_damage(weapon):
    pass
```
в результате возвращает количество урона

###  health

##### Описание
выводит жизни в зависимости от выбора

##### Функция
```Python
def count_health(armor):
    pass
```
в результате возвращает количество жизней

### bonus damage

##### Описание
выводит бонусный урон в зависимости от выбора

##### Функция
```Python
def count_bonus_damage(skill):
    pass
```
в результате возвращает количество бонусного урона

### bonus health

##### Описание
выводит бонусные жизни в зависимости от выбора

##### Функция
```Python
def count_bonus_health(accessory):
    pass
```
в результате возвращает количество бонусных жизней


