# Тема 8. Введение в ООП
Отчет по Теме #8 выполнил:
- Леганьков Иван Сергеевич
- ИВТ-22-2

| Задание | Лаб_раб | Сам_раб|
| ------ | ------ | ------|
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |


знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.


Лабораторные задания:	

1) Создайте класс "Car" с атрибутами производитель и модель. Создайте объект этого класса. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями.

```python
class Car: #класс Car представляет автомобиль
    def __init__(self, make, model): #метод __init__ служит для инициализации объекта
        self.make = make #присвоение значений свойствам объекта
        self.model = model
my_car = Car("Daewoo", "Nexia") #создание объекта my_car класса Car, передавая параметры "Toyota" и  "Corolla"
#эти значения будут присвоены свойствам make  и model объекта my_car
```
![Меню](https://github.com/Kamui76/Prorammnaya_Ingeneria/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%208%20%D0%BB%D0%B0%D0%B1%D0%B0%20%D0%9F%D0%98/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B51.png)
- Данная программа создает класс 'Car' с атрибутами, после создаётся объект класса


2) Дополните код из первого задания, добавив в него атрибуты и методы класса, заставьте машину “поехать". Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
class Car: #класс Car представляет автомобиль
    def __init__(self, make, model): #метод __init__ служит для инициализации объекта
        self.make = make #присвоение значений свойствам объекта
        self.model = model
    def drive(self): # Метод drive описывает поведение автомобиля при вождении
        print(f"Driving the {self.make} {self.model}") # Вывод сообщения о том, какая машина управляется
my_car = Car("Daewoo", "Nexia") #создание объекта my_car класса Car, передавая параметры "Daewoo" и  "Nexia"
#эти значения будут присвоены свойствам make  и model объекта my_car
my_car.drive() # Вызов метода drive для объекта my_car
```
![Меню](https://github.com/Kamui76/Prorammnaya_Ingeneria/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%208%20%D0%BB%D0%B0%D0%B1%D0%B0%20%D0%9F%D0%98/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B52.png)
- Данная программа добавляет в программу из прошлого задания атрибуты и методы класса, заставляет машину “поехать"

3) Создайте новый класс "ElectricCar" с методом "charge" и атрибутом емкость батареи. Реализуйте его наследование от класса, созданного в первом задании. Заставьте машину поехать, а потом заряжаться.
Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
```python
class Car:  # класс Car представляет автомобиль
    def __init__(self, make, model):  # метод __init__ служит для инициализации объекта
        self.make = make  # присвоение значений свойствам объекта
        self.model = model

    def drive(self):  # метод drive описывает поведение автомобиля при вождении
        print(f"Driving the {self.make} {self.model}")  # вывод сообщения о том, какая машина управляется


my_car = Car("Daewoo", "Nexia")  # создание объекта my_car класса Car, передавая параметры "Daewoo" и  "Nexia"
# эти значения будут присвоены свойствам make  и model объекта my_car
my_car.drive()  # вызов метода drive для объекта my_car


class ElectricCar(Car):  # класс ElectricCar представляет электромобиль
    def __init__(self, make, model, battery_capacity):  # метод __init__ служит для инициализации объекта
        super().__init__(make, model)  # наследуем свойства make и model от родительского класса Car
        self.battery_capacity = battery_capacity  # присваиваем емкость аккумулятора свойству battery_capacity

    def charge(self):  # метод charge описывает процесс зарядки электромобиля
        print(
            f"Charging the {self.make} {self.model} with {self.battery_capacity} kWh")  # вывод сообщения о процессе зарядки


my_electric_car = ElectricCar("Tesla", "Model X",
                              75)  # создание объекта my_electric_car класса ElectricCar с параметрами "Tesla", "Model X" и 75
my_electric_car.drive()  # вызов метода drive для объекта my_electric_car
my_electric_car.charge()  # вызов метода charge для объекта my_electric_car
```
![Меню](https://github.com/Kamui76/Prorammnaya_Ingeneria/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%208%20%D0%BB%D0%B0%D0%B1%D0%B0%20%D0%9F%D0%98/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B53.png)
- Данная программа создает новый класс "ElectricCar" с методом "charge" и атрибутом емкость батареи


4) Реализуйте инкапсуляцию для класса, созданного в первом задании. Создайте защищенный атрибут производителя и приватный атрибут модели. Вызовите защищенный атрибут и заставьте машину поехать. Напишите комментарии для кода, объясняющие его работу.
Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
class Car: #класс Car представляет автомобиль
    def __init__(self, make, model): #метод __init__ служит для инициализации объекта
        self._make = make #защищенный атрибут
        self.__model = model #приватный атрибут
    def drive(self): # метод drive описывает поведение автомобиля при вождении
        print(f"Driving the {self._make} {self.__model}") # вывод сообщения о том, какая машина управляется
my_car = Car("Daewoo", "Nexia") #создание объекта my_car класса Car, передавая параметры "Daewoo" и  "Nexia"
#эти значения будут присвоены свойствам make  и model объекта my_car
print(my_car._make) #доступ к защищённому атрибуту
my_car.drive() # вызов метода drive для объекта my_car
```
![Меню](https://github.com/Kamui76/Prorammnaya_Ingeneria/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%208%20%D0%BB%D0%B0%D0%B1%D0%B0%20%D0%9F%D0%98/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B54.png)
- Данная программа реализует инкапсуляцию для класса


5) Реализуйте полиморфизм создав основной (общий) класс "Shape", а также еще два класса "Rectangle” и “Circle”. Внутри последних двух классов реализуйте методы для подсчета площади фигуры. После этого создайте массив с фигурами, поместите туда круг и прямоугольник, затем при помощи цикла выведите их площади. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
# Класс Shape является базовым классом для всех геометрических фигур.
class Shape:# Метод area() объявлен абстрактным методом, который будет переопределен в дочерних классах.
    def area(self):
        pass
# Класс Rectangle наследует от класса Shape и представляет прямоугольник.
class Rectangle(Shape):
    # Конструктор инициализирует ширину и высоту прямоугольника.
    def __init__(self, width, height):
        self.width = width
        self.height = height
    # Метод area() вычисляет площадь прямоугольника как произведение ширины на высоту.
    def area(self):
        return self.width * self.height
# Класс Circle наследует от класса Shape и представляет круг.
class Circle(Shape):
    # Конструктор инициализирует радиус круга.
    def __init__(self, radius):
        self.radius = radius
    # Метод area() вычисляет площадь круга по формуле
    def area(self):
        return 3.14 * self.radius ** 2
```
![Меню](https://github.com/Kamui76/Prorammnaya_Ingeneria/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%208%20%D0%BB%D0%B0%D0%B1%D0%B0%20%D0%9F%D0%98/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B55.png)
- Данная программа реализует полиморфизм создав основной (общий) класс "Shape", а также еще два класса "Rectangle” и “Circle”

Самостоятельные задания:

1) Самостоятельно создайте класс и его объект. Они должны
отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Games:
    def __init__(self, title, author, limit):
        self.title = title
        self.developer = author
        self.agelimit = limit
    def game_info(self):
        print(f'Название игры: {self.title}')
        print(f'Разработчик: {self.developer}')
        print(f'Ограничение по возрасту: {self.agelimit}')
game1 = Games('GTA5', 'Rockstar games', 18)
game1.games_info()
```
![Меню](https://github.com/Kamui76/Prorammnaya_Ingeneria/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%208%20%D0%BB%D0%B0%D0%B1%D0%B0%20%D0%9F%D0%98/%D0%A1%D0%B0%D0%BC%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B51.png)
- Данная программа создает класс и его объект
2) Самостоятельно создайте атрибуты и методы для ранее созданного класса. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Games:
    def __init__(self, title, author, limit, genre, progress):
        self.title = title
        self.developer = author
        self.agelimit = limit
        self.genre = genre
        self.progress = progress
    def game_info(self):
        print(f'Название игры: {self.title}')
        print(f'Разработчик: {self.developer}')
        print(f'Ограничение по возрасту: {self.agelimit}')
        print(f'Жанр: {self.genre}')
        print(f'Прогресс прохождения: {self.progress}')

        def reset_progress(self):
            self.progress = 0
            print('Вы начали игру заново.')
game1 = Games('GTA5', 'Rockstar games', 18, 'RPG', '27%')
game1.game_info()
```
![Меню](https://github.com/Kamui76/Prorammnaya_Ingeneria/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%208%20%D0%BB%D0%B0%D0%B1%D0%B0%20%D0%9F%D0%98/%D0%A1%D0%B0%D0%BC%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B52.png)
- Данная программа создает атрибуты и методы для ранее созданного класса 

3) Самостоятельно реализуйте наследование, продолжая работать с ранее созданным классом. Оно должно отличаться, от того, что указано в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Games:
    def __init__(self, title, author, limit, genre=None, progress=None):
        self.title = title
        self.developer = author
        self.agelimit = limit
        self.genre = genre
        self.progress = progress
    def game_info(self):
        print(f'Название игры: {self.title}')
        print(f'Разработчик: {self.developer}')
        print(f'Ограничение по возрасту: {self.agelimit}')
        print(f'Жанр: {self.genre}')
        print(f'Прогресс прохождения: {self.progress}')

        def reset_progress(self):
            self.progress = 0
            print('Вы начали игру заново.')
game1 = Games('GTA5', 'Rockstar games', 18, 'RPG', '27%')
game1.game_info()

class OGames(Games):
    def __init__(self, title, author, limit, type, genre=None, progress=None):
        super().__init__(self, title, author, limit, genre, progress)
        self.type = type
    def ogames_info(self):
        super().game_info()
        print(f'Тип игры: {self.type}')
ogame1 = OGames('Паук', 'Microsoft', 0, 'Предустановленная', 'Карточная', '0%')
ogame1.ogames_info()
```
![Меню](https://github.com/Kamui76/Prorammnaya_Ingeneria/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%208%20%D0%BB%D0%B0%D0%B1%D0%B0%20%D0%9F%D0%98/%D0%A1%D0%B0%D0%BC%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B53.png)
- Данная программа реализует наследование

4) Самостоятельно реализуйте инкапсуляцию, продолжая работать с ранее созданным классом. Она должна отличаться, от того, что указана в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
```python
class Games:
    def __init__(self, title, author, lvl, genre=None, progress=None):
        self.title = title
        self.developer = author
        self.lvl = lvl
        self.genre = genre
        self.progress = progress
    def game_info(self):
        print(f'Название игры: {self.title}')
        print(f'Разработчик: {self.developer}')
        print(f'Текущий уровень: {self.lvl}')
        print(f'Жанр: {self.genre}')
        print(f'Прогресс прохождения: {self.progress}')
    def reset_lvl(self):
        self.lvl = 0
        print('Вы нанчали игру заново')
    def title(self):
        return self._title
    def title(self, value):
        self._title = value
    def author(self):
        return self._author
    def author(self, value):
        self._author = value
    def pages(self):
        return self._lvl
    def pages(self, value):
        if value > 0:
            self._lvl = value
        else:
            raise ValueError("Номер уровня должен быть положительным")
    def lvl(self):
        return self._lvl
    def genre(self):
        return self._genre
    def genre(self, value):
        self._genre = value
    def progress(self):
        return self._progress
    def progress(self, value):
        self._progress = value
class OGames(Games):
    def __init__(self, title, author, lvl, type, genre=None, progress=None):
        super().__init__(title, author, lvl, genre, progress)
        self.type = type
    def egame_info(self):
        super().game_info()
        print(f'Тип игры: {self.type}')
    def file_format(self):
        return self._file_format
    def file_format(self, value):
        self._file_format = value
game1 = Games('GTA5', 'Rockstar games', 18, 'RPG', '27%')
game1.game_info()
egame1 = OGames('Паук', 'Microsoft', 0, 'Предустановленная', 'Карточная', '0%')
egame1.egame_info()
```
![Меню](https://github.com/Kamui76/Prorammnaya_Ingeneria/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%208%20%D0%BB%D0%B0%D0%B1%D0%B0%20%D0%9F%D0%98/%D0%A1%D0%B0%D0%BC%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B54.png)
-Данная программа реализует инкапсуляцию

5) Самостоятельно реализуйте полиморфизм. Он должен отличаться, от того, что указан в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
```python
class Games:
    def __init__(self, title, author, lvl, genre=None, progress=None):
        self.title = title
        self.developer = author
        self.lvl = lvl
        self.genre = genre
        self.progress = progress
    def display_info(self):
        print(f'Название игры: {self.title}')
        print(f'Разработчик: {self.developer}')
        print(f'Текущий уровень: {self.lvl}')
        print(f'Жанр: {self.genre}')
        print(f'Прогресс прохождения: {self.progress}')
    def reset_lvl(self):
        self.lvl = 0
        print('Вы нанчали игру заново')
    def title(self):
        return self._title
    def title(self, value):
        self._title = value
    def author(self):
        return self._author
    def author(self, value):
        self._author = value
    def pages(self):
        return self._lvl
    def pages(self, value):
        if value > 0:
            self._lvl = value
        else:
            raise ValueError("Номер уровня должен быть положительным")
    def lvl(self):
        return self._lvl
    def genre(self):
        return self._genre
    def genre(self, value):
        self._genre = value
    def progress(self):
        return self._progress
    def progress(self, value):
        self._progress = value
class OGames(Games):
    def __init__(self, title, author, lvl, type, genre=None, progress=None):
        super().__init__(title, author, lvl, genre, progress)
        self.type = type
    def egame_info(self):
        super().game_info()
        print(f'Тип игры: {self.type}')
    def file_format(self):
        return self._file_format
    def file_format(self, value):
        self._file_format = value
def display_game_info(book):
    book.display_info()

game1 = Games('GTA5', 'Rockstar games', 18, 'RPG', '27%')
egame1 = OGames('Паук', 'Microsoft', 0, 'Предустановленная', 'Карточная', '0%')

display_game_info(game1)
display_game_info(egame1)
```
![Меню](https://github.com/Kamui76/Prorammnaya_Ingeneria/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%208%20%D0%BB%D0%B0%D0%B1%D0%B0%20%D0%9F%D0%98/%D0%A1%D0%B0%D0%BC%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B55.png)
- Данная программа реализует полиморфизм
