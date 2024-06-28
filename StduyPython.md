# python基础

## 1.变量和简单的数据类型

**变量只能由字母、数字和下划线组成。**

**在python中，只要有操作数是浮点数，默认得到的总是浮点数，即便原来为整数。**

### 1.1 添加空白

```python
print("python")
print("\npython")
print("\tpython")
```

### 1.2 删除空白

```python
favorite_language = ' python '
print(favorite_language.rstrip())		# 删除右空白
print(favorite_language.lstrip())		# 删除左空白
print(favorite_language.strip())		# 同时删除两边的空白
```

### 1.3 删除前缀

```python
nostarch_url = 'http://nostarch.com'
nostarch_url.removeprefix('http://')
```

### 1.4 首字母大写

```python
name = "ada lovelace"
print(name.title())
```

## 2.列表

### 2.1 修改元素

```python
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

motorcycles[0] = 'ducati'
print(motorcycles)
```

### 2.2 添加元素

#### 2.2.1 在列表末尾添加元素

```python
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

motorcycles.append('ducati')
print(motorcycles)
```

#### 2.2.2 在列表插入元素

```
motorcycles = ['honda', 'yamaha', 'suzuki']

motorcycles.insert(0, 'ducati')
print(motorcycles)
```

### 2.3 删除元素

#### 2.3.1 删除末尾的元素

```python
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

popped_motorcycle = motorcycles.pop()
```

#### 2.3.2 删除任意位置的元素

```python
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

del motorcycles[0]
del motorcycles[1]
print(motorcycles)
```

#### 2.3.3 根据值删除元素

```python
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
print(motorcycles)

motorcycles.remove('ducati')		# 使用remove()从列表中删除元素后，也可继续使用它的值
print(motorcycles)					# remove()只删除第一个指定的值
```

### 2.4 管理元素

#### 2.4.1 sort()

```python
cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.sort()						# sort()方法永久地修改列表元素的排列顺序
cars.sort(reverse=True)			# 按反方向顺序排列
print(cars)
```

#### 2.4.2 sorted()

```python
cars = ['bmw', 'audi', 'toyota', 'subaru']

print("\nHere is the sorted list:")
print(sorted(cars))				# 调用sorted()后列表元素没有变
```

### 2.5 反向打印元素

```python
cars = ['bmw', 'audi', 'toyota', 'subaru']

cars.reverse()
print(cars)
```

### 2.6 列表长度

```python
cars = ['bmw', 'audi', 'toyota', 'subaru']
print(len(cars))
```

### 2.7 遍历列表

```python
magicians = ['alice', 'david', 'carolina']
for magician in magicians:
    print(f"{magician.title()}, that was a great trick!")
    print(f"I can't wait to see your next trick, {magician.title()}.\n")

print("Thank you, everyone. That was a great magic show!")
```

### 2.8 数值列表

```python
squares = []
for value in range(1, 11):		# 不包含第二个值
    squares.append(value**2)	# ** 表示平方

print(squares)
```

### 2.9 数值统计计算

```
digits = [1, 2, 3, 4, 5, 6, 7, 8, 9]
print(min(digits))		# 最小
print(max(digits))		# 最大
print(sum(digits))		# 总计
```

### 2.10 切片

```python
players = ['charles', 'martina', 'michael', 'florence', 'eli']

print("Here are the first three players on my team:")
for player in players[:3]:
    print(player.title())
```

### 2.11 复制列表

```python
my_foods = ['pizza', 'falafel', 'carrot cake']
friend_foods = my_foods[:]
```

## 3.元组

### 3.1 定义元组

```python
dimensions = (200, 50)
print(dimensions[0])
print(dimensions[1])

dimension = (3,)	# 只包含一个元素时必须在元素后面加上逗号
```

### 3.2 遍历元组

```python
dimensions = (200, 50)
for dimension in dimensions:
    print(dimension)
```

## 4.If语句

```python
age = 12
if age < 4:
    price = 0
elif age < 18:
    price = 25
elif age < 65:
    price = 40
else:
    price = 20

print(f"Your admission cost is ${price}.")
```

## 5.字典

### 5.1 添加键值对

```python
alien_0 = {'color': 'green', 'points': 5}

alien_0['x_position'] = 0
alien_0['y_position'] = 25
print(alien_0)
```

### 5.2 修改字典值

```python
alien_0 = {'color': 'green'}
print(f"The alien is {alien_0['color']}.")

alien_0['color'] = 'yellow'
print(f"The alien is now {alien_0['color']}.")
```

### 5.3 删除键值对

```python
alien_0 = {'color': 'green', 'points': 5}
print(alien_0)

del alien_0['points']
print(alien_0)
```

### 5.4 get()来访问值

```python
alien_0 = {'color': 'green', 'speed': 'slow'}

point_value = alien_0.get('points', 'No point value.')		# 调用get()时，如果没有指定第二个参数则返回值None
print(point_value)
```

### 5.5 遍历字典

#### 5.5.1 遍历所有键

```python
favorite_languages = {'jen':'python','sarah':'c','edward':'rust','phil':'python'}
for name in favorite_languages.keys():
    print(name.title())
```

#### 5.5.2 遍历所有值

```python
favorite_languages = {'jen':'python','sarah':'c','edward':'rust','phil':'python'}

for language in favorite_languages.values():
    print(language.title())
```

#### 5.5.3 遍历所有键值对

```python
user_0 = {'username': 'efermi','first': 'enrico','last': 'fermi'}

for key, value in user_0.items():
    print(f"\nKey: {key}")
    print(f"Value: {value}")
```

### 5.6嵌套

```python
users = {
    'aeinstein': {'first': 'albert','last': 'einstein','location': 'princeton'},
    'mcurie': {'first': 'marie','last': 'curie','location': 'paris'},
    }

for username, user_info in users.items():
    print(f"\nUsername: {username}")
    full_name = f"{user_info['first']} {user_info['last']}"
    location = user_info['location']
    
    print(f"\tFull name: {full_name.title()}")
    print(f"\tLocation: {location.title()}")
```

## 6.while循环

### 6.1 使用标志

```python
prompt = "\nTell me something, and I will repeat it back to you:"

active = True
while active:
    message = input(prompt)
    if message == 'quit':
        active = False
    else:
        print(message)
```

### 6.2 使用break

```
prompt = "\nPlease enter the name of a city you have visited:"

while True:
    city = input(prompt)

    if city == 'quit':
        break		# 遇到break语句直接退出循环
    else:
        print(f"I'd love to go to {city.title()}!")
```

### 6.3 使用continue

```python
current_number = 0
while current_number < 10:
    current_number += 1
    if current_number % 2 == 0:
        continue

    print(current_number)
```

### 6.4 处理列表和字典

#### 6.4.1 在列表之间移动元素

```python
unconfirmed_users = ['alice', 'brian', 'candace']
confirmed_users = []

while unconfirmed_users:
    current_user = unconfirmed_users.pop()
    print(f"Verifying user: {current_user.title()}")
    confirmed_users.append(current_user)

print("\nThe following users have been confirmed:")
for confirmed_user in confirmed_users:
    print(confirmed_user.title())
```

#### 6.4.2 删除为特定值的所有列表元素

```python
pets = ['dog', 'cat', 'dog', 'goldfish', 'cat', 'rabbit', 'cat']
print(pets)

while 'cat' in pets:
    pets.remove('cat')

print(pets)
```

#### 6.4.3 使用用户输入填充字典

```python
responses = {}
polling_active = True

while polling_active:
    name = input("\nWhat is your name? ")
    response = input("Which mountain would you like to climb someday? ")
    responses[name] = response

    repeat = input("Would you like to let another person respond? (yes/ no) ")
    if repeat == 'no':
        polling_active = False

for name, response in responses.items():
    print(f"{name} would like to climb {response}.")
```

## 7.函数

### 7.1 定义函数

```python
def greet_user():
    print("Hello!")
    
greet_user()
```

### 7.2 传递实参

#### 7.2.1 位置实参

```python
def describe_pet(animal_type, pet_name):
    print(f"\nI have a {animal_type}.")
    print(f"My {animal_type}'s name is {pet_name.title()}.")	

describe_pet('hamster', 'harry')	# 位置不同带入的值不同
describe_pet('harry', 'hamster')	
```

#### 7.2.2 关键字实参

```python
def describe_pet(animal_type, pet_name):
    print(f"\nI have a {animal_type}.")
    print(f"My {animal_type}'s name is {pet_name.title()}.")

describe_pet(animal_type='hamster', pet_name='harry')
```

#### 7.2.3 默认值

```python
def describe_pet(pet_name, animal_type='dog'):	# 当使用默认值时，必须先列出没有默认值的形参，再列出默认值的形参
    print(f"\nI have a {animal_type}.")
    print(f"My {animal_type}'s name is {pet_name.title()}.")

describe_pet(pet_name='willie')
```

#### 7.2.4 传递任意数量实参

```python
def make_pizza(size, *toppings):	# *让python创建一个名为toppings的元组，该元组包含函数收到的所有值
    print(f"\nMaking a {size}-inch pizza with the following toppings:")
    for topping in toppings:
        print(f"- {topping}")

make_pizza(16, 'pepperoni')
make_pizza(12, 'mushrooms', 'green peppers', 'extra cheese')
```

#### 7.2.5 使用任意数量的关键字实参

```python
def build_profile(first, last, **user_info):    # **让python创建一个名为user_info的字典，该字典包含函数所有键值对
    user_info['first_name'] = first
    user_info['last_name'] = last
    return user_info

user_profile = build_profile('albert', 'einstein',
                             location='princeton',
                             field='physics')
print(user_profile)
```

### 7.3 模块

#### 7.3.1 导入特定函数

```python
from moudle_name import function_name
```

#### 7.3.2 使用as指定别名

```python
from pizza import make_pizza as mp
```

#### 7.3.3 导入模块中所有函数

```python
from pizza import *
```

## 8.类

### 8.1 创建类

```python
class Dog:
    def __init__(self, name, age):					# 类中的函数称为方法 __init__ 是一种特殊的方法
        self.name = name
        self.age = age

    def sit(self):
        print(f"{self.name} is now sitting.")

    def roll_over(self):
        print(f"{self.name} rolled over!")

my_dog = Dog('Willie', 6)
my_dog.sit()				# 调用方法
my_dog.roll_over()
```

### 8.2 使用类

```python
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.odometer_reading = 0			# 指定默认值

    def get_descriptive_name(self):
        long_name = f"{self.year} {self.make} {self.model}"
        return long_name.title()

    def read_odometer(self):
        print(f"This car has {self.odometer_reading} miles on it.")

my_new_car = Car('audi', 'a4', 2024)
print(my_new_car.get_descriptive_name())
my_new_car.read_odometer()
```

### 8.3 修改类中属性值

#### 8.3.1 直接修改

```python
my_new_car.odometer_reading = 23
my_new_car.read_odometer()
```

#### 8.3.2 通过方法修改

```python
	def update_odometer(self, mileage):
      	self.odometer_reading = mileage
        
my_new_car.update_odometer(23)
my_new_car.read_odometer()
```

### 8.4 继承

```python
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.odometer_reading = 0
    def get_descriptive_name(self):
        long_name = f"{self.year} {self.make} {self.model}"
        return long_name.title()
    def read_odometer(self):
        print(f"This car has {self.odometer_reading} miles on it.")
    def update_odometer(self, mileage):
        if mileage >= self.odometer_reading:
            self.odometer_reading = mileage
        else:
            print("You can't roll back an odometer!")
    def increment_odometer(self, miles):
        self.odometer_reading += miles
class ElectricCar(Car):						# ElectricCar具有Car父类的功能
    def __init__(self, make, model, year):
        super().__init__(make, model, year)		# super()函数用来调用父类的方法
        self.battery_size = 40

    def describe_battery(self):
        print(f"This car has a {self.battery_size}-kWh battery.")

my_leaf = ElectricCar('nissan', 'leaf', 2024)
print(my_leaf.get_descriptive_name())
my_leaf.describe_battery()
```

### 8.5 导入类

```python
from car import Car								# 导入一个类

from car import Car, ElectricCar				# 导入多个类

import car										# 导入整个模块

from car import *								# 导入模块中所有类

from car import Car
from electric_car import ElectricCar			# 在一个模块中导入另一个模块

from electric_car import ElectricCar as EC		# 使用别名
my_new_car = Car('audi', 'a4', 2024)
print(my_new_car.get_descriptive_name())

my_new_car.odometer_reading = 23
my_new_car.read_odometer()
```

## 9.文件

### 9.1 读取文件

```python
from pathlib import Path

path = Path('pi_digits.txt')
contents = path.read_text()

lines = contents.splitlines()		# splitlines()方法将冗长的字符串转换成一系列行
for line in lines:
  print(line)
```

### 9.2 写入文件

```python
from pathlib import Path

contents = "I love programming.\n"
contents += "I love creating new games.\n"
contents += "I also love working with data.\n"

path = Path('programming.txt')
path.write_text(contents)				# python只能将字符串写入文件
```

### 9.3 json

#### 9.3.1 json.dumps()

```python
from pathlib import Path
import json

numbers = [2, 3, 5, 7, 11, 13]

path = Path('numbers.json')
contents = json.dumps(numbers)			# 存储数据
path.write_text(contents)
```

#### 9.3.2 json.loads()

```python
from pathlib import Path
import json

path = Path('numbers.json')
contents = path.read_text()
numbers = json.loads(contents)			# 传递数据

print(numbers)
```

## 10.异常

```python
print("Give me two numbers, and I'll divide them.")
print("Enter 'q' to quit.")

while True:
    first_number = input("\nFirst number: ")
    if first_number == 'q':
        break
    second_number = input("Second number: ")
    if second_number == 'q':
        break
    try:
        answer = int(first_number) / int(second_number)
    except ZeroDivisionError:			# 出现代码的错误
        print("You can't divide by 0!")
    else:
        print(answer)
```

## 11.测试

### 11.1 安装pytest

```python
python -m pip install pytest
```

### 11.2 测试函数

```python
from name_function import get_formatted_name

def test_first_last_name():						# 测试文件名称必须以test_打头
    formatted_name = get_formatted_name('janis', 'joplin')
    assert formatted_name == 'Janis Joplin'		# assert为断言

def test_first_last_middle_name():
    formatted_name = get_formatted_name(
        'wolfgang', 'mozart', 'amadeus')
    assert formatted_name == 'Wolfgang Amadeus Mozart'
```

### 11.3 夹具

```python
import pytest
from survey import AnonymousSurvey

@pytest.fixture				# 夹具帮助搭建测试环境
def language_survey():
    question = "What language did you first learn to speak?"
    language_survey = AnonymousSurvey(question)
    return language_survey

def test_store_single_response(language_survey):
    language_survey.store_response('English')
    assert 'English' in language_survey.responses

def test_store_three_responses(language_survey):
    responses = ['English', 'Spanish', 'Mandarin']
    for response in responses:
        language_survey.store_response(response)

    for response in responses:
        assert response in language_survey.responses
```

# python进阶

## 第1章 Python数据模型

### 1.1 一摞Python风格的纸牌

```python
import collections

Card = collections.namedtuple('Card', ['rank', 'suit'])
# 也可以用分割的字符串 Card = collections.namedtuple('Card', "rank,suit")
class FrenchDeck:
    ranks = [str(n) for n in range(2, 11)] + list('JQKA')
    suits = 'spades diamonds clubs hearts'.split()

    def __init__(self):
        self._cards = [Card(rank, suit) for suit in self.suits for rank in self.ranks]

    def __len__(self):
        return len(self._cards)

    def __getitem__(self, position):	# __getitem__(self,key)这个方法返回所给键对应的值
        return self._cards[position]
# 指定一张纸牌
beer_card = Card('7', 'diamondes')
beer_card
# 计算一摞纸牌的张数
deck = FrenchDeck()
len(deck)
# 抽取第一张
deck[0]
# 抽取最后一张
deck[-1]

from random import choice
# 随机选择一张牌
choice(deck)
# 只抽最上面三张
print(deck[:3])
# 从索引12开始，即跳过13张牌，只抽取4张A
print(deck[12::13])
```

### 1.2 特殊方法是如何使用的

```python
import math

class Vector:
    def __init__(self, x=0, y=0):
        self.x = x
        self.y = y

    def __repr__(self):
        # !r与%r的转换字段一致
        return f'Vector({self.x!r}, {self.y!r})'

    def __abs__(self):
        return math.hypot(self.x, self.y)	# hypot()返回欧几里德范数 sqrt(x*x + y*y)。

    def __bool__(self):
        return bool(abs(self))

    def __add__(self, other):
        x = self.x + other.x
        y = self.y + other.y
        return Vector(x, y)

    def __mul__(self, scalar):
        return Vector(self.x * scalar, self.y * scalar)
```

## 第2章 丰富的序列

### 2.1 列表推导式和生成器表达式

#### 2.1.1 列表推导式对可读性的影响

```python
# 基于字符串构建一个Unicode码点列表
symbols = '$%^&*'
codes = []
for symbol in symbols:
    codes.append(ord(symbol))

# 使用列表推导式基于一个字符串构建一个Unicode码点列表
symbols = '$%^&*'
codes = [ord(symbol) for symbol in symbols]
```

#### 2.1.2 列表推导式与map和filter比较

```python
# 使用列表推导式和map/filter组合构建同一个列表
symbols = '$%^&*'
beyond_ascii = [ord(s) for s in symbols if ord(s) > 36]

beyond_ascii = list(filter(lambda c: c > 36, map(ord, symbols)))	# lambda是匿名函数 
											  # filter()函数用于过滤序列，过滤掉不符合条件的元素，返回一个迭代器对象
```

#### 2.1.3 海象运算符

```python
x = 'ABC'
condes = [last := ord(c) for c in x] # :=相当于for c in x: last = ord(c)
print(last)
```

#### 2.1.4 生成器表达式

```python
# 使用生成器表达式构建一个元组和数组
symbols = '$%^&*'
tuple(ord(symbol) for symbol in symbols)


import array	# array函数把列表转换成数组
print(array.array('I', (ord(symbol) for symbol in symbols)))
# 使用生成器表达式计算笛卡尔积
colors = ['black', 'white']
sizes = ['S', 'M', 'L']
for tshirt in (f'{c} {s}' for c in colors for s in sizes):
    print(tshirt)
```

### 2.2 元组不仅仅是不可变列表

#### 2.2.1把元组当作记录使用

```python
lax_coordinates = (33.9425, -118.408056)
city, year, pop, chg, area = ('Tokyo', 2003, 32_450, 0.66, 8014)
traveler_ids = [('USA', '31195855'), ('BRA', 'CE243567'), ('ESP', 'XDA205856')]
for country, _ in traveler_ids:		# _表示虚拟变量，当前一个命令结果不是None则赋值给_			
    print(country)
```

### 2.3 序列和可迭代对象拆包

#### 2.3.1 并行赋值

```python
lax_coordinates = (33.9425, -118.408056)
latitude, longitude = lax_coordinates	# 拆包 并行赋值

divmod(20,8)	# (a // b, a % b)
t = (20,8)
print(divmod(*t))
```

#### 2.3.2 使用*获取余下的项

并行赋值时，*前缀只能应用到一个变量上，可以是任何位置上的变量。

```python
a, b, *rest = range(5)
>>>(0, 1, [2, 3, 4])
a, *body, c, d = range(5)
>>>(0, [1, 2], 3, 4)
```

#### 2.3.3嵌套拆包

```python
metro_areas = [
    ('Tokyo', 'JP', 36.933, (35.689722, 139.691667)),
    ('Delhi NCR', 'IN', 21.935, (28.613889, 77.208889)),
    ('Mexico City', 'MX', 20.142, (19.433333, -99.133333)),
    ('New York-Newark', 'US', 20.104, (40.808611, -74.020386)),
    ('Sao Paulo', 'BR', 19.649, (-23.547778, -46.635833))
]
def main():
	print(f'{"":15} | {"latitude":>9} | {"longitude":>9}')
	for name, _, _, (lat, lon) in metro_areas:	# 把最后一个字段赋给嵌套元组
    	if lon <= 0:
        	print(f'{name:15} | {lat:9.4f} | {lon:9.4f}')
>>>             |  latitude | longitude
Mexico City     |   19.4333 |  -99.1333
New York-Newark |   40.8086 |  -74.0204
Sao Paulo       |  -23.5478 |  -46.6358
```

### 2.3 序列模式匹配

```python
metro_areas = [
    ('Tokyo', 'JP', 36.933, (35.689722, 139.691667)),
    ('Delhi NCR', 'IN', 21.935, (28.613889, 77.208889)),
    ('Mexico City', 'MX', 20.142, (19.433333, -99.133333)),
    ('New York-Newark', 'US', 20.104, (40.808611, -74.020386)),
    ('Sao Paulo', 'BR', 19.649, (-23.547778, -46.635833))
]
def main():
	print(f'{"":15} | {"latitude":>9} | {"longitude":>9}')
	for record in metro_areas:
   		match record: 
        	case [name, _, _, (lat, lon)] if lon <= 0:		# 如果有case _表示前面都不匹配时执行
              	print(f'{name:15} | {lat:9.4f} | {lon:9.4f}')
>>>             |  latitude | longitude
Mexico City     |   19.4333 |  -99.1333
New York-Newark |   40.8086 |  -74.0204
Sao Paulo       |  -23.5478 |  -46.6358
```

匹配序列模式的条件：

1. 匹配对象是序列。
2. 匹配对象和模式的项数相等。
3. 对应的项相互匹配，包括嵌套的项。

### 2.4 切片

```python
# 从纯文本形式的发票中提取商品信息
invoice = """
0.....6.................................40........52...55........
1909  Pimoroni PiBrella                     $17.50    3    $52.50
1489  6mm Tactile Switch x20                 $4.95    2     $9.90
1510  Panavise Jr. - PV-201                 $28.00    1    $28.00
1601  PiTFT Mini Kit 320x240                $34.95    1    $34.95
"""
SKU = slice(0, 6)
DESCRIPTION = slice(6, 40)
UNIT_PRICE = slice(40, 52)
QUANTITY = slice(52, 55)
ITEM_TOTAL = slice(55, None)
line_items = invoice.split('\n')[2:]
for item in line_items:
    print(item[UNIT_PRICE], item[DESCRIPTION])
    
>>> $17.50   Pimoroni PiBrella                 
     $4.95   6mm Tactile Switch x20            
    $28.00   Panavise Jr. - PV-201             
    $34.95   PiTFT Mini Kit 320x240   
    
# 切片赋值
l = list(range(10))
>>>l
[0,1,2,3,4,5,6,7,8,9]
>>>l[2:5] = [20, 30]
>>>l
[0,1,20,30,5,6,7,8,9]
>>>del l[5:7]
>>>l
[0,1,20,30,5,8,9]
```

### 2.5 当列表不适用时

#### 2.5.1 数组

如果一个列表只包含数值，使用`array.array`会更高效。

```python
from array import array
from random import random
# 创建一个双精度浮点数数组
floats = array('d', (random() for i in range(10**7)))	# 创建双精度浮点数数组
floats[-1]	
>>>0.4197427599509004
# 把数组存入一个二进制文件中
fp = open('floats.bin', 'wb')
floats.tofile(fp)		# tofile()将数组中的数据以二进制格式写进文件
fp.close()
# 从二进制文件中读取1000万个数
floats2 = array('d')
fp = open('floats.bin', 'rb')
floats2.fromfile(fp, 10**7)		# fromfile()函数读回数据时需要用户指定元素类型，并对数组的形状进行适当的修改
fp.close()
floats2[-1]
>>>0.4197427599509004
floats2 == floats
>>>True
```

#### 2.5.2 memoryview)

内置的menoryview类是一种共享内存的序列类型，可在不复制字节的情况下处理数组的切片。

- 分别以1x6、2x3和3x2矩阵的视图处理6字节内存

```python
from array import array

octets = array('B', range(6))
m1 = memoryview(octets)
print(m1.tolist())			# tolist()用于将数组或矩阵转为列表
>>>[0, 1, 2, 3, 4, 5]
# 构建2x3的矩阵
m2 = m1.cast('B', [2,3])	# cast是指数据类型转换，其目的是将一个变量或值从一种数据类型转换为另一种数据类型
print(m2.tolist())
>>>[[0, 1, 2], [3, 4, 5]]
# 构建3x2的矩阵
m3 = m1.cast('B', [3, 2])
print(m3.tolist())
>>>[[0, 1], [2, 3], [4, 5]]
# octets、m1、m2、m3之间的内存是共享的
m2[1,1] = 22
m3[1,1] = 33
print(octets)
>>>array('B', [0, 1, 2, 33, 22, 5])
```

- 修改一个16位整数数组中某一项的字节，改变该项的值

```python
numbers = array('h', [-2, -1, 0, 1, 2])
memv = memoryview(numbers)
print(len(memv))
>>>5
print(memv[0])
>>>-2
memv_oct = memv.cast('B')
print(memv_oct.tolist())
>>>[254, 255, 255, 255, 0, 0, 1, 0, 2, 0]
memv_oct[5] = 4
print(numbers)
>>>array('h', [-2, -1, 1024, 1, 2])
```

#### 2.5.3 双端队列和其他队列

- deque类实现一种线程安全的双端队列，旨在快速在两端插入和删除项。
- queue提供几个同步（即线程安全）队列类，在队列填满后，阻塞插入新项，等待其他线程从队列中取出一项。
- multiprocessiong单独实现了无界SimpleQueue和有界的Queue。
- asyncio提供了Queue、LifoQueue、PriorityQueue和JoinableQueue，为管理异步编程任务而做了修改。

```python
# 处理一个deque对象
from collections import deque

dq = deque(range(10), maxlen=10)
print(dq)
>>>deque([0, 1, 2, 3, 4, 5, 6, 7, 8, 9], maxlen=10)
# 轮转。当n>0时，从右端取几项放到左端，当n<0时，从左端取几项放到右端。
dq.rotate(3)
print(dq)
>>>deque([7, 8, 9, 0, 1, 2, 3, 4, 5, 6], maxlen=10)
dq.rotate(-4)
print(dq)
>>>deque([1, 2, 3, 4, 5, 6, 7, 8, 9, 0], maxlen=10)
# 在已满的队列中的一端追加，另一端要丢弃
dq.appendleft(-1)
print(dq)
>>>deque([-1, 1, 2, 3, 4, 5, 6, 7, 8, 9], maxlen=10)
dq.extend([11, 22, 33])
print(dq)
>>>deque([3, 4, 5, 6, 7, 8, 9, 11, 22, 33], maxlen=10)
dq.extendleft([10, 20, 30, 40])
print(dq)
>>>deque([40, 30, 20, 10, 3, 4, 5, 6, 7, 8], maxlen=10)
```

## 第3章 字典和集合

### 3.1 字典的现代句法

#### 3.1.1字典推导式

```python
dial_codes = [
    (880, 'Bangladesh'),
    (55, 'Brazil'),
    (86, 'China'),
    (91, 'India'),
    (62, 'Indonesia'),
    (81, 'Japan'),
    (234, 'Nigeria'),
    (92, 'Pakistan'),
    (7, 'Russia'),
    (1, 'United States'),
]
# 对调键和值
country_dial = {country: code for code, country in dial_codes}
>>>country_dial
{'Bangladesh': 880,'Brazil': 55,'China': 86,'India': 91,'Indonesia': 62,'Japan': 81,'Nigeria': 234,
 'Pakistan': 92,'Russia': 7,'United States': 1}
# 按国家名称排序，再次对调键和值，把值转成大写，筛选code<70的项
{code: country.upper()
    for country, code in sorted(country_dial.items())
    if code < 70}
>>>{55: 'BRAZIL', 62: 'INDONESIA', 7: 'RUSSIA', 1: 'UNITED STATES'}
```

#### 3.1.2映射拆包

```python
def dump(**kwargs):
    return kwargs

dump(**{'x' :1}, y=2, **{'z': 3})
>>>{'x': 1, 'y': 2, 'z': 3}
{'a': 0, **{'x': 1}, 'y': 2, **{'z': 3, 'x': 4}}
>>>{'a': 0, 'x': 4, 'y': 2, 'z': 3}
```

#### 3.1.3使用`|`合并映射

```python
d1 = {'a': 1, 'b': 3}
d2 = {'a': 2, 'b': 4, 'c': 6}
d1 | d2
>>>{'a': 2, 'b': 4, 'c': 6}
```

### 3.2 使用模式匹配处理映射

```python
# 从出版物记录中提取创作者的名字
def get_creators(record: dict) -> list:		# 表面参数为一个dict返回值是一个list
    match record:
        case {'type': 'book', 'api': 2, 'authors': [*names]}:
            return names
        case {'type': 'book', 'api': 1, 'author': name}:
            return [name]
        case {'type': 'book'}:
            return ValueError(f"Invalid 'book' record: {record!r}")
        case {'type': 'movie', 'director': name}:
            return [name]
        case _:
            return ValueError(f'Invalid record: {record!r}')
b1 = dict(api=1, author='Douglas Hofstadter', type='book', title='Godel, Escher, Bach')
get_creators(b1)
>>>['Douglas Hofstadter']
from collections import OrderedDict

b2 = OrderedDict(api=2, type='book', title='Python in a Nutshell', authors='Martelli Ravenscroft Holden'.split())
get_creators(b2)
>>>['Martelli', 'Ravenscroft', 'Holden']
```

### 3.3 自动处理丢失的键

```python
# 在查找键时把非字符串键转换成字符串
class StrKeyDict0(dict):
    def __missing__(self, key):
        if isinstance(key, str):
            raise KeyError(key)
        return self[str(key)]
    
    def get(self, key, default=None):
        try:
            return self[key]
        except KeyError:
            return default
        
    def __contains__(self, key):
        return key in self.keys() or str(key) in self.keys()
# 搜索非字符串键时，StrKeyDict0把未找到的键转换成字符串    
>>>d = StrKeyDict0([('2', 'two'), ('4', 'four')])
>>>d['2']
'two'
>>>d[4]
'four'
>>>d.get('2')
'two'
>>>d.get(4)
'four'
>>>d.get(1, 'N/A')
'N/A'
```

### 3.4 dict的变体

1.collections.OrderedDict

- 等值检查考虑顺序
- 方便执行重新排序操作，空间利用率、迭代速度和更新操作的性能是次要的。
- 从算法上看，OrderedDict处理频繁重新排序操作的效果比dict好，适合用于跟踪近期存取情况。

2.collections.ChainMap

- 存放一组映射，可作为一个整体来搜索。
- 查找操作按照输入映射在构造函数调用中出现的顺序执行，一旦找到指定的键，立即结束。
- 不复制输入映射，存放映射的引用。
- 更新或插入操作只影响第一个输入映射。

3.collections.Counter

- 一种对键计数的映射，更新现有的键，计数随之增加。
- 可用于统计可哈希对象的实例数量。

4.shelve.Shelf

- 持久存储字符串键与Python对象之间的映射。

```python
# StrKeyDict在插入、更新和查找时，始终把非字符串键转换为str类型
import collections

class StrKeyDict(collections.UserDict):		# StrKeyDict扩展UserDict
    def __missing__(self, key):
        if isinstance(key, str):
            raise KeyError(key)
        return self[str(key)]
    
    def __contains__(self, key):
        return str(key) in self.data
    
    def __setitem__(self, key, item):
        self.data[str(key)] = item
```

### 3.5 不可变映射

```python
#从MappingProxyType根据dict对象构建只读的mappingproxy实例
from types import MappingProxyType

d = {1: 'A'}
d_proxy = MappingProxyType(d)
d_proxy
mappingproxy({1: 'A'})
print(d_proxy[1])
>>>'A'
d[2] = 'B'
print(d_proxy)
>>>mappingproxy({1: 'A', 2: 'B'})
print(d_proxy[2])
>>>'B'
```

### 3.6 集合论

集合的基本作用是去除重复项。

```python
l = ['spam', 'spam', 'eggs', 'spam', 'bacon', 'eggs']
print(set(l))
>>>{'bacon', 'eggs', 'spam'}
print(list(set(l)))
>>>['bacon', 'eggs', 'spam']
# 如果想要去除重复项，同时保留每一项首次出现位置的顺序
>>>list(dict.fromkeys(l).keys()		
>>>['spam', 'eggs', 'bacon']
# fromkeys()函数用于创建一个新字典，以序列 seq 中元素做字典的键，value 为字典所有键对应的初始值
>>> dict1={}
>>> dict1.fromkeys((1,2,3),'number')
{1: 'number', 2: 'number', 3: 'number'}
>>> print(dict1)
{}
>>> dict2=dict1.fromkeys((1,2,3),'number')
>>> dict2
{1: 'number', 2: 'number', 3: 'number'}         
# 集合推导式
from unicodedata import name

print({chr(i) for i in range(32, 256) if 'SIGN' in name(chr(i), '')})
>>>{'×', '%', '>', '¥', '§', '¬', '=', '°', '¶', '©', '¢', 'µ', '±', '#', '¤', '£', '$', '÷', '®', '<', '+'}
```

## 第4章 Unicode文本和字节序列

### 4.1 字符问题

- 字符的标识：码点，是0~1114111范围内的数（十进制），在Unicode标准中以4~6个十六进制数表示，前面加“U+”，取值范围是U+0000~U+10FFFF。
- 字符的具体描述取决于所用的编码。编码是在码点和字节序列之间转换时使用的算法。

```python
# 编码和解码
>>>s = 'café'
>>>len(s)
4
>>>b = s.encode('utf8')		# 把str对象编码成bytes对象
>>>b, len(b)
(b'caf\xc3\xa9', 5)
>>>b.decode('utf8')			# 把bytes对象编码成str对象
'café'
```

### 4.2 字节概要

```python
# 包含5个字节的bytes和bytearray对象
>>>cafe = bytes('café', encoding='utf_8')
>>>cafe
b'caf\xc3\xa9'
>>>cafe[0], cafe[:1]
(99, b'c')
>>>cafe_arr = bytearray(cafe)
>>>cafe_arr, cafe_arr[-1:]
(bytearray(b'caf\xc3\xa9'), bytearray(b'\xa9'))
```

### 4.3 处理编码和解码问题

#### 4.3.1处理UnicodeEncodeError

```python
# 把str编码成字节序列，有些成功，有些需要处理错误
>>>city = 'Sāo Paulo'
>>>city.encode('utf_8')
b'S\xc4\x81o Paulo'
>>>city.encode('utf_16')
b'\xff\xfeS\x00\x01\x01o\x00 \x00P\x00a\x00u\x00l\x00o\x00'
>>>city.encode('iso8859_1', errors='ignore')
b'So Paulo'
>>>city.encode('cp437', errors='replace')
b'S?o Paulo'
>>>city.encode('cp437', errors='xmlcharrefreplace')
b'S&#257;o Paulo'
```

#### 4.3.2处理UnicodeDecodeError

```python
# 把字节序列解码成str，有些成功，有些需要处理错误
>>>octets = b'Montr\xe9al'
>>>octets.decode('cp1252')
'Montréal'
>>>octets.decode('iso8859_7')
'Montrιal'
>>>octets.decode('koi8_r')
'MontrИal'
>>>octets.decode('utf_8', errors='replace')
'Montr�al'
```

### 4.4 默认编码

```python
import locale
import sys

expressions = """
        locale.getpreferredencoding()
        type(my_file)
        my_file.encoding
        sys.stdout.isatty()
        sys.stdout.encoding
        sys.stdin.isatty()
        sys.stdin.encoding
        sys.stderr.isatty()
        sys.stderr.encoding
        sys.getdefaultencoding()
        sys.getfilesystemencoding()
    """

my_file = open('dummy', 'w')

for expression in expressions.split():
    value = eval(expression)
    print(f'{expression:>30} -> {value!r}')
 locale.getpreferredencoding() -> 'cp936'
                 type(my_file) -> <class '_io.TextIOWrapper'>
              my_file.encoding -> 'cp936'
           sys.stdout.isatty() -> False
           sys.stdout.encoding -> 'UTF-8'
            sys.stdin.isatty() -> False
            sys.stdin.encoding -> 'gbk'
           sys.stderr.isatty() -> False
           sys.stderr.encoding -> 'UTF-8'
      sys.getdefaultencoding() -> 'utf-8'
   sys.getfilesystemencoding() -> 'utf-8'
```

### 4.5 为了正确比较而规范化Unicode字符

- NFC（Normalization Form C）：使用最少的码点构成等价的字符串。
- NFD：把合成字符分解成基字符和单独的组合字符。

```python
>>>from unicodedata import normalize
>>>s1 = 'café'
>>>s2 = 'cafe\N{COMBINING ACUTE ACCENT}'
>>>len(s1), len(s2)
(4, 5)
>>>len(normalize('NFC', s1)), len(normalize('NFC', s2))		# normalize函数规范化字符串
(4, 4)
>>>len(normalize('NFD', s1)), len(normalize('NFD', s2))
(5, 5)
```

### 4.6 极端“规范化”：去掉变音符

```python
import unicodedata

def shave_marks(txt):
    """删除所有变音符"""
    # 把所有字符分解成基字符和组合记号
    norm_txt = unicodedata.normalize('NFD', txt)
    # 过滤所有组合记号
    shaved = ''.join(c for c in norm_txt
                     if not unicodedata.combining(c))
    # 重组所有字符
    return unicodedata.normalize('NFC', shaved)
>>>order = '“Herr Voß: • ½ cup of Œtker™ caffè latte • bowl of açaí.”'
>>>shave_marks(order)
'“Herr Voß: • ½ cup of Œtker™ caffe latte • bowl of acai.”'
>>>greek = 'Ζέφυρος, Zéfiro'
>>>shave_marks(greek)
'Ζεφυρος, Zefiro'
# 删除拉丁字母中组合记号的函数
import string

def shave_marks_latin(txt):
    """删除所有拉丁基字符上的变音符"""
    norm_txt = unicodedata.normalize('NFD', txt)
    latin_base = False
    preserve = []
    for c in norm_txt:
        if unicodedata.combining(c) and latin_base:
            continue  # 忽略拉丁基字符的变音符
        preserve.append(c)
        # 如果不是组合字符，那就是新的基字符
        if not unicodedata.combining(c):
            latin_base = c in string.ascii_letters
    shaved = ''.join(preserve)
    return unicodedata.normalize('NFC', shaved)
# 把西方印刷字符转换成ASCII字符
single_map = str.maketrans("""‚ƒ„ˆ‹‘’“”•–—˜›""","""'f"^<''""---~>""")
multi_map = str.maketrans({  
    '€': 'EUR',
    '…': '...',
    'Æ': 'AE',
    'æ': 'ae',
    'Œ': 'OE',
    'œ': 'oe',
    '™': '(TM)',
    '‰': '<per mille>',
    '†': '**',
    '‡': '***',
})
multi_map.update(single_map)  # 合并两个映射表

def dewinize(txt):
    """把cp1252符号替换为ASCII字符或字符序列"""
    return txt.translate(multi_map)
def asciize(txt):
    # 去掉变音符
    no_marks = shave_marks_latin(dewinize(txt))
    no_marks = no_marks.replace('ß', 'ss')
    # 使用NFKC规范化形式把字符和码点组合起来
    return unicodedata.normalize('NFKC', no_marks)
>>>order = '“Herr Voß: • ½ cup of Œtker™ caffè latte • bowl of açaí.”'
>>>dewinize(order)
'"Herr Voß: - ½ cup of OEtker(TM) caffè latte - bowl of açaí."'
>>>asciize(order)
'"Herr Voss: - 1⁄2 cup of OEtker(TM) caffe latte - bowl of acai."'
```

### 4.7 Unicode文本排序

```python
# 巴西产水果的列表排序
import locale
my_locale = locale.setlocale(locale.LC_COLLATE, 'pt_BR.UTF-8')
fruits = ['caju', 'atemoia', 'cajá', 'açaí', 'acerola']
print(sorted(fruits, key=locale.strxfrm))
>>>['açaí', 'acerola', 'atemoia', 'cajá', 'caju']
```

### 4.8 Unicode数据库

Unicode标准提供了一个完整的数据库，不仅包括码点与字符名称之间的映射表，还包括各个字符的元数据，以及字符之间的关系。

- unicodedata.name()：返回一个字符在标准中的官方名称
- unicodedata.numeric()：返回一个字符在标准中的数值

### 4.9 支持str和bytes的双模式API

#### 4.9.1 正则表达式中的str和bytes

```python
import re

# str类型
re_numbers_str = re.compile(r'\d+')
re_words_str = re.compile(r'\w+')
# bytes类型
re_numbers_bytes = re.compile(rb'\d+')
re_words_bytes = re.compile(rb'\w+')

text_str = ("Ramanujan saw \u0be7\u0bed\u0be8\u0bef"
            " as 1729 = 1³ + 12³ = 9³ + 10³.")

# bytes正则表达式只能搜索bytes字符串
text_bytes = text_str.encode('utf_8')

print(f'Text\n  {text_str!r}')
print('Numbers')
# str模式r'\d+'只能匹配泰米尔数值和ASCII数字
print('  str  :', re_numbers_str.findall(text_str)) 
# bytes模式rb'\d+'只能匹配ASCII字节中的数字
print('  bytes:', re_numbers_bytes.findall(text_bytes))  
print('Words')
# str模式r'\w+'能匹配字母、上标、泰米尔数字和ASCII数字
print('  str  :', re_words_str.findall(text_str))  
# bytes模式rb'\w+'只能匹配ASCII字节中的字母和数字
print('  bytes:', re_words_bytes.findall(text_bytes)) 
>>>Text
  'Ramanujan saw ௧௭௨௯ as 1729 = 1³ + 12³ = 9³ + 10³.'
Numbers
  str  : ['௧௭௨௯', '1729', '1', '12', '9', '10']
  bytes: [b'1729', b'1', b'12', b'9', b'10']
Words
  str  : ['Ramanujan', 'saw', '௧௭௨௯', 'as', '1729', '1³', '12³', '9³', '10³']
  bytes: [b'Ramanujan', b'saw', b'as', b'1729', b'1', b'12', b'9', b'10']
```

#### 4.9.2 os函数中的str和bytes

- `os`模块中所有接收文件名或路径名的函数，既可以传入`str`参数，也可以传入`bytes`参数。
- 传入`str`参数时，使用`sys.getfilesystemencoding()`获得的编码解码器自动转换参数，操作系统回显时也使用编码解码器进行解码。
- `os`模块提供了特殊的编码解码函数`os.fsencode(name_or_path)`和`os.fsdecode(name_or_path)`。

## 第5章 数据类构建器

### 5.1 数据类构建器概述

#### 5.1.1直接通过类构建

```python
# 表示地理位置的经纬度
class Coordinate:
    def __init__(self, lat, lon):
        self.lat = lat
        self.lon = lon
>>>moscow = Coordinate(55.76, 37.62)
>>>location = Coordinate(55.76, 37.62)
>>>location == moscow
False
>>>(location.lat, location.lon) == (moscow.lat, moscow.lon)
True
```

#### 5.1.2使用namedtuple构建Coordinate类

```python
>>>from collections import namedtuple

>>>Coordinate = namedtuple('Coordinate', 'lat lon')
>>>issubclass(Coordinate, tuple)
True
>>>moscow = Coordinate(55.76, 37.62)
>>>moscow == Coordinate(lat=55.76, lon=37.62)
True
```

#### 5.1.3使用typing.NamedTuple构建

```python
from typing import NamedTuple

class Coordinate(NamedTuple):
    lat: float
    lon: float

    def __str__(self):
        ns = 'N' if self.lat >= 0 else 'S'
        we = 'E' if self.lon >= 0 else 'W'
        return f'{abs(self.lat):.1f}°{ns}, {abs(self.lon):.1f}°{we}'
```

#### 5.1.4使用dataclass装饰器声明实例属性

```python
from dataclasses import dataclass

@dataclass(frozen=True)		# dataclass 生成的类是可变的。如果希望生成不可变的类，可以在类定义中添加 frozen=True
class Coordinate:
    lat: float
    lon: float

    def __str__(self):
        ns = 'N' if self.lat >= 0 else 'S'
        we = 'E' if self.lon >= 0 else 'W'
        return f'{abs(self.lat):.1f}°{ns}, {abs(self.lon):.1f}°{we}'
```

### 5.2 典型的具名元组

#### 5.2.1定义并使用一个具名元组类型

```python
>>>from collections import namedtuple

>>>City = namedtuple('City', 'name country population coordinates')
>>>tokyo = City('Tokyo', 'JP', 36.933, (35.689722, 139.691667))
>>>tokyo
City(name='Tokyo', country='JP', population=36.933, coordinates=(35.689722, 139.691667))
>>>tokyo.population, tokyo.coordinates, tokyo[1]
(36.933, (35.689722, 139.691667), 'JP')
```

#### 5.2.2具名元组的属性和方法

```python
>>>City._fields		# ._fileds属性的值是一个元组，存储类的字段名称
('name', 'country', 'population', 'coordinates')
>>>Coordinate = namedtuple('Coordinate', 'lat lon')
>>>delhi_data = ('Delhi NCR', 'IN', 21.935, Coordinate(28.613889, 77.208889))
>>>delhi = City._make(delhi_data)	# ._make()方法根据可迭代对象构建City实列
>>>delhi._asdict()	# ._asdict()方法返回根据具名元组实列构建的dict对象
{'name': 'Delhi NCR',
 'country': 'IN',
 'population': 21.935,
 'coordinates': Coordinate(lat=28.613889, lon=77.208889)}
>>>import json

>>>json.dumps(delhi._asdict())	# ._asdict()方法可把数据序列化成JSON格式
'{"name": "Delhi NCR", "country": "IN", "population": 21.935, "coordinates": [28.613889, 77.208889]}'
```

#### 5.2.3构建一个具名元组，为字段指定默认值

```python
>>>Coordinate = namedtuple('Coordinate', 'lat lon reference', defaults=['WSG84']) 
>>>Coordinate(0, 0)
Coordinate(lat=0, lon=0, reference='WSG84')
>>>Coordinate._field_defaults
{'reference': 'WSG84'}
```

### 5.3 @dataclass详解

#### 5.3.1@dataclass定义

@dataclass(*, init=True, repr=True, eq=True, order=False, unsafe_hash=False, frozen=False)

- init：默认值是True，生成__init__，如果用户自己实现了__init__，则忽略该参数。
- repr：默认值是True，生成__repr__，如果用户自己实现了__repr__，则忽略该参数。
- eq：默认值是True，生成__eq__，如果用户自己实现了__eq__，则忽略该参数。
- order：默认值是False，生成__lt__、__le__、__gt__、__ge__、如果eq=False，或者执行定义或继承其他用于比较的方法，则抛出异常。
- unsafe_hase：默认值是False，生成__hash__。
- frozen：默认值是False，让实例不可变。

```python
# 定义ClubMember
from dataclasses import dataclass, field

@dataclass
class ClubMember:
    name: str
    guests: list = field(default_factory=list)    
```

#### 5.3.2都柏林核心模式

都柏林核心模式是一小组术语，可用于描述数字资源(视频、图像、网页等)，也可用于描述物理资源，例如图书、CD和艺术品等对象。

```python
from dataclasses import dataclass, field, fields
from typing import Optional
from enum import Enum, auto
from datetime import date

class ResourceType(Enum):  
    BOOK = auto()
    EBOOK = auto()
    VIDEO = auto()

@dataclass
class Resource:
    """描述媒体资源"""
    identifier: str                                   
    title: str = '<untitled>'                          
    creators: list[str] = field(default_factory=list)
    date: Optional[date] = None                        
    type: ResourceType = ResourceType.BOOK             
    description: str = ''
    language: str = ''
    subjects: list[str] = field(default_factory=list)
        
    def __repr__(self):
        cls = self.__class__
        cls_name = cls.__name__
        indent = ' ' * 4
        res = [f'{cls_name}(']		# 声明构建输出字符串的res列表，把第一项设为类名和左圆括号                     
        for f in fields(cls):                             
            value = getattr(self, f.name)                 
            res.append(f'{indent}{f.name} = {value!r},')  
        res.append(')')                                   
        return '\n'.join(res)                             
>>>description = 'Improving the design of existing code'
>>>book = Resource('978-0-13-475759-9', 'Refactoring, 2nd Edition', 
                ['Martin Fowler', 'Kent Beck'], date(2018, 11, 19),
                ResourceType.BOOK, description, 'EN',
                ['computer programming', 'OOP'])
>>>book		# doctest: +NORMALIZE_WHITESPACE
Resource(
    identifier = '978-0-13-475759-9',
    title = 'Refactoring, 2nd Edition',
    creators = ['Martin Fowler', 'Kent Beck'],
    date = datetime.date(2018, 11, 19),
    type = <ResourceType.BOOK: 1>,
    description = 'Improving the design of existing code',
    language = 'EN',
    subjects = ['computer programming', 'OOP'],
)
```

## 第6章 对象引用、可变性和垃圾回收

### 6.1 默认做浅拷贝

浅拷贝的方式：

- 复制列表使用内置的类型构造函数。
- 使用`[:]`进行浅拷贝。
- 使用`copy.copy`函数进行浅拷贝。

```python
l1 = [3, [66, 55, 44], (7, 8, 9)]
l2 = list(l1)		# l2是l1的浅拷贝
l1.append(100)		# 把100追加到l1中，l2不受影响
l1[1].remove(55)	# 把内部列表l1[1]中的55删除，这对l2有影响
print('l1:', l1)
>>>l1: [3, [66, 44], (7, 8, 9), 100]
print('l2:', l2)
>>>l2: [3, [66, 44], (7, 8, 9)]
l2[1] += [33, 22]	# 添加在列表中对l1有影响
l2[2] += (10, 11)	# 添加在元组中对l1无影响
print('l1:', l1)
>>>l1: [3, [66, 44, 33, 22], (7, 8, 9), 100]
print('l2:', l2)
>>>l2: [3, [66, 44, 33, 22], (7, 8, 9, 10, 11)]
```

深拷贝方式：使用`copy.deepcopy`函数

```python
# 校车乘客在途中有上有下
class Bus:
    def __init__(self, passengers=None):
        if passengers is None:
            self.passengers = []
        else:
            self.passengers = list(passengers)

    def pick(self, name):
        self.passengers.append(name)

    def drop(self, name):
        self.passengers.remove(name)
>>>import copy
>>>bus1 = Bus(['Alice', 'Bill', 'Claire', 'David'])
# 使用浅拷贝
>>>bus2 = copy.copy(bus1)
# 使用深拷贝
>>>bus3 = copy.deepcopy(bus1)
>>>bus1.drop('Bill')
>>>bus2.passengers
['Alice', 'Claire', 'David']
>>>bus3.passengers
['Alice', 'Bill', 'Claire', 'David']
```

### 6.2 函数的参数是引用时

```python
# 函数可能会修改接收到的任何可变对象
>>>def f(a,b):
		a += b
        return a
>>>x = 1
>>>y = 2
>>>f(x,y)
3
>>>x, y
(1, 2)
>>>a = [1, 2]
>>>b = [3, 4]
>>>f(a, b)
[1, 2, 3, 4]
>>>a, b
([1, 2, 3, 4], [3, 4])
>>>t = (10, 20)
>>>u = (30, 40)
>>>f(t, u)
(10, 20, 30, 40)
>>>t, u
((10, 20), (30, 40))
```

#### 6.2.1 不要使用可变类型作为参数的默认值

```python
class HauntedBus:
	def __init__(self, passengers=[]):
        self.passengers = passengers
    def pick(self, name):
        self.passengers.append(name)
    def drop(self, name):
        self.passengers.remove(name)
>>>bus1 = HauntedBus(['Alice','Bill'])
>>>bus1.passengers
['Alice','Bill']
>>>bus1.pick('Charlie')
>>>bus1.drop('Alice')
>>>bus1.passengers
['Bill', 'Charlie']
>>>bus2 = HauntedBus()
>>>bus2.pick('Carrie')
>>>bus2.passengers
['Carrie']
>>>bus3 = HauntedBus()
>>>bus3.passengers()
['Carrie']
>>>bus3.pick('Dave')
>>>bus3.passengers
['Carrie', 'Dave']
>>>bus2.passengers is bus3.passengers
True
>>>bus1.passengers
['Bill', 'Charlie']
```

#### 6.2.2 防御可变参数

```python
class TwilightBus:
    """让乘客销声匿迹的校车"""
    def __init__(self, passengers=None):
        if passengers is None:
            self.passengers = []  
        else:
            # WARN：不能直接引用变量，应使用浅拷贝
            self.passengers = passengers

    def pick(self, name):
        self.passengers.append(name)

    def drop(self, name):
        self.passengers.remove(name)
basketball_team = ['Sue', 'Tina', 'Maya', 'Diana', 'Pat']
bus = TwilightBus(basketball_team)
bus.drop('Tina')
bus.drop('Pat')
# 下车的学生从篮球队中消失了！
>>>basketball_team
['Sue', 'Maya', 'Diana']
# 修改后的代码
class TwilightBus:
    """让乘客销声匿迹的校车"""
    def __init__(self, passengers=None):
        if passengers is None:
            self.passengers = []  
        else:
            # 使用构造器的浅拷贝方式
            self.passengers = list(passengers)		# 创建passengers列表的副本，如果不是列表就把它转换成列表

    def pick(self, name):
        self.passengers.append(name)

    def drop(self, name):
        self.passengers.remove(name)
```

## 第7章 函数是一等对象

### 7.1 把函数视为对象

```python
# 创建并测试一个函数
def factorial(n):
    """return n!"""
    return 1 if n < 2 else n * factorial(n - 1)
fact = factorial
>>>fact(5)
120
list(map(factorial, range(11)))
>>>[1, 1, 2, 6, 24, 120, 720, 5040, 40320, 362880, 3628800]
```

- 将函数赋值给变量，通过变量名调用。
- 把函数作为参数传给`map`函数，返回一个可迭代对象。

### 7.2 高阶函数

- map的替代：使用列表推导式。
- filter的替代：在列表推导式中使用`if`过滤。
- reduce的替代：使用内置函数，比如`sum`、`all`、`any`等。

### 7.3 9种可调用对象

- 用户定义的函数：使用`def`语句或`lambda`表达式创建的函数。
- 内置函数：例如`len`或`time.strftime`。
- 内置方法：例如`dict.get`。
- 方法：在类主体中定义的函数。
- 类：调用类时运行类的`__new__`方法创建一个实例，然后运行`__init__`方法，初始化实例，最后把实例返回给调用方。
- 类的实例：如果定义了`__call__`方法，实例可以作为函数调用。
- 生成器函数：主体中有`yield`关键字的函数或方法，返回一个生成器对象。
- 原生协程函数：使用`async def`定义的函数或方法，返回一个协程对象。
- 异步生成器函数：使用`async def`定义，而且主体中有`yield`关键字的函数或方法，返回一个异步生成器，供`async for`使用。

### 7.4 仅限关键字参数

```python
def tag(name, *content, class_=None, **attrs):
    """生成一个或多个HTML标签"""
    if class_ is not None:
        attrs['class'] = class_
    attr_pairs = (f' {attr}="{value}"' for attr, value
                    in sorted(attrs.items()))
    attr_str = ''.join(attr_pairs)
    if content:
        elements = (f'<{name}{attr_str}>{c}</{name}>'
                    for c in content)
        return '\n'.join(elements)
    else:
        return f'<{name}{attr_str} />'
# 传入单个位置参数
>>>tag('br')
'<br />'
# 第一个参数后面的任意数量的参数被*content捕获，存入一个元组
>>>tag('p', 'hello')
'<p>hello</p>'
# tag函数签名中没有明确指定名称的关键字参数被**attrs捕获，存入一个字典
>>>tag('p', 'hello', id=3)
'<p id="3">hello</p>'
# class_参数智能作为关键字参数传入
>>>print(tag('p', 'hello', 'world', class_='sidebar'))
<p class="sidebar">hello</p>
<p class="sidebar">world</p>
# 第一个位置参数也能作为关键字参数传入
>>>tag(content='testing', name='img')
'<img content="testing" />'
# 加上**之后，字典中的所有项作为参数依次传入
>>>my_tag = {'name': 'img', 'title': 'Sunset Boulevard',
           'src': 'sunset.jpg', 'class': 'framed'}
>>>tag(**my_tag)
'<img class="framed" src="sunset.jpg" title="Sunset Boulevard" />'
```

### 7.5 支持函数式编程的包

#### 7.5.1 operator模块

```python
# 使用reduce函数和operator.mul函数计算阶乘
from functools import reduce
from operator import mul

def factorial(n):
    return reduce(mul, range(1, n + 1))
# 使用itemgetter排序一个元组列表
>>>metro_data = [
    ('Tokyo', 'JP', 36.933, (35.689722, 139.691667)),  
    ('Delhi NCR', 'IN', 21.935, (28.613889, 77.208889)),
    ('Mexico City', 'MX', 20.142, (19.433333, -99.133333)),
    ('New York-Newark', 'US', 20.104, (40.808611, -74.020386)),
    ('São Paulo', 'BR', 19.649, (-23.547778, -46.635833)),
]
>>>
>>>from operator import itemgetter		# itemgetter根据元组的某个字段对元组列表进行排序
>>>for city in sorted(metro_data, key=itemgetter(1)):
...    print(city)Copy to clipboardErrorCopied
('São Paulo', 'BR', 19.649, (-23.547778, -46.635833))
('Delhi NCR', 'IN', 21.935, (28.613889, 77.208889))
('Tokyo', 'JP', 36.933, (35.689722, 139.691667))
('Mexico City', 'MX', 20.142, (19.433333, -99.133333))
('New York-Newark', 'US', 20.104, (40.808611, -74.020386))
>>>cc_name = itemgetter(1, 0)
>>>for city in metro_data:
...    print(cc_name(city))
('JP', 'Tokyo')
('IN', 'Delhi NCR')
('MX', 'Mexico City')
('US', 'New York-Newark')
('BR', 'São Paulo')
# 使用attrgetter处理定义的具名元组metro_data
>>>from collections import namedtuple
>>>LatLon = namedtuple('LatLon', 'lat lon')
>>>Metropolis = namedtuple('Metropolis', 'name cc pop coord')
>>>metro_areas = [Metropolis(name, cc, pop, LatLon(lat, lon)) 
...    for name, cc, pop, (lat, lon) in metro_data]
>>>metro_areas[0]
Metropolis(name='Tokyo', cc='JP', pop=36.933, coord=LatLon(lat=35.689722, lon=139.691667))
>>>metro_areas[0].coord.lat
35.689722
>>>from operator import attrgetter
>>>name_lat = attrgetter('name', 'coord.lat')
>>>for city in sorted(metro_areas, key=attrgetter('coord.lat')):
...    print(name_lat(city))
('São Paulo', -23.547778)
('Mexico City', 19.433333)
('Delhi NCR', 28.613889)
('Tokyo', 35.689722)
('New York-Newark', 40.808611)
# 使用methodcaller
>>>from operator import methodcaller
>>>s = 'The time has come'
>>>upcase = methodcaller('upper')
>>>upcase(s)
'THE TIME HAS COME'
>>>hyphenate = methodcaller('replace', ' ', '-')
>>>hyphenate(s)
'The-time-has-come'
```

#### 7.5.2 使用functools.partial冻结参数

```python
# 使用partial把一个双参数函数改造成只需要一个参数的可调用对象
>>>from operator import mul
>>>from functools import partial	# partial中的第一个参数表示可调用参数
>>>triple = partial(mul, 3)		# mul(a, b)表示a*b
>>>triple(7)
21
>>>list(map(triple, range(1, 10)))
[3, 6, 9, 12, 15, 18, 21, 24, 27]
```

## 第8章 函数中的类型提示

### 8.1 渐进式类型

- 渐进式类型系统的性质：
  1. 是可选的：默认情况下，类型检查工具不应对没有类型提示的代码发出警告。如果无法确定对象的类型时，会假定为Any类型。
  2. 不在运行时捕获类型错误：在运行时不能阻止把不一致的值传给函数或分配给变量。
  3. 不能改善性能。

### 8.2 类型由受支持的操作定义

- 鸭子类型：对象有类型，但变量（包括参数）没有类型。为对象声明的类型无关紧要，重要的是对象具体支持什么操作。比名义类型更灵活，但代价是运行时潜在的错误更多。
- 名义类型：对象只存在于运行时，类型检查工具只关心使用类型提示注解变量（包括参数）的源码。比鸭子类型更严格，优点是能在构建流水线中，甚至在IDE中输入代码的过程中更早地捕获一些bug。

### 8.3 注解中可用的类型

- typing.Any类型：动态类型
  1. 对T1及其子类型T2，T2与T1相容（里氏替换原则）
  2. 任何类型都与Any相容。
  3. Any与任何类型都相容。
- 简单的类型和类：例如int、float、str和bytes这样的简单的类型可以直接在类型提示中使用。
- Optional类型和Union类型：`Union[]`至少需要两种类型，嵌套的Union类型与扁平的Union类型效果相同。
- 泛化容器：泛型可以用类型参数来声明，以指定可以处理的项的类型。例如，`list[str]`。
- 元组类型：
  1. 用作记录的元组，例如：`tuple[str, float, str]`。
  2. 带有具名字段，用作记录的元组，使用`typing.NamedTuple`。
  3. 用作不可变序列的元组，例如：`tuple[Any,...]`。
- 泛化映射：使用`MappingType[KeyType, ValueType]`形式注解。

```python
import sys
import re
import unicodedata
from collections.abc import Iterator

RE_WORD = re.compile(r'\w+')
STOP_CODE = sys.maxunicode + 1

def tokenize(text: str) -> Iterator[str]:  
    """返回全大写的单词构成的可迭代对象"""
    for match in RE_WORD.finditer(text):
        yield match.group().upper()

def name_index(start: int = 32, end: int = STOP_CODE) -> dict[str, set[str]]:
    index: dict[str, set[str]] = {}  
    for char in (chr(i) for i in range(start, end)):
        # 使用海象运算符，进行结果赋值
        if name := unicodedata.name(char, ''):  
            for word in tokenize(name):
                index.setdefault(word, set()).add(char)
    return index
>>>index = name_index(32, 65)
>>>index['SIGN']
{'#', '$', '%', '+', '<', '=', '>'}
>>>index['DIGIT']
{'0', '1', '2', '3', '4', '5', '6', '7', '8', '9'}
>>>index['DIGIT'] & index['EIGHT']
{'8'}
```

- 抽象基类：一般来说，在参数得类型提示中最好使用`abc.Mapping`或`abc.MutableMapping`，不要使用`dict`。
- Iterable：使用`collections.abc`包中的`Iterable`。

```python
from collections.abc import Iterable

FromTo = tuple[str, str]	# 类型别名
def zip_replace(text: str, changes: Iterable[FromTo]) -> str: 
    for from_, to in changes:
        text = text.replace(from_, to)
    return text
>>>l33t = [('a', '4'), ('e', '3'), ('i', '1'), ('o', '0')]
>>>text = 'mad skilled noob powned leet'
>>>from replacer import zip_replace
>>>zip_replace(text, l33t)
'm4d sk1ll3d n00b p0wn3d l33t'
```

- 参数化泛型和TypeVar：参数化泛型`list[T]`，其中`T`是类型变量，而密匙使用时会绑定具体的类型。

```python
from collections.abc import Sequence
from random import shuffle
from typing import TypeVar

# 定义泛型参数
T = TypeVar('T')

def sample(population: Sequence[T], size: int) -> list[T]:
    if size < 1:
        raise ValueError('size must be >= 1')
    result = list(population)
    shuffle(result)
    return result[:size]
```

- 静态协议（typing.Protocols）：协议通过`typing.Protocols`的子类定义，类型检查工具负责查找可用的协议类型，施行用法检查。

```python
# 使用bound=SupportsLessThan的TypeVar定义top函数
from collections.abc import Iterable
from typing import TypeVar
from typing import Protocol, Any

class SupportsLessThan(Protocol):
    def __lt__(self, other: Any) -> bool: 
        pass


LT = TypeVar('LT', bound=SupportsLessThan)

def top(series: Iterable[LT], length: int) -> list[LT]:
    ordered = sorted(series, reverse=True)
    return ordered[:length]
>>>top([4, 1, 5, 2, 6, 7, 3], 3)
[7, 6, 5]
>>>l = 'mango pear apple kiwi banana'.split()
>>>top(l, 3)
['pear', 'mango', 'kiwi']
```

- Callable：用于注解回调参数或高阶函数返回的可调用对象。
- NoReturn：仅用于注解绝不返回的函数的返回值类型。这类函数通常会抛出异常。

### 8.4 类型检查工具的缺点

- 一些便利的功能无法做静态检查，比如`config(**settings)`这种参数拆包。
- 对特性、描述符、元类和元编程等高级功能的支持很差，或者根本无法理解。
- 跟不上Python版本的变化，可能拒绝使用语言新特性的代码，甚至崩溃。

## 第9章 装饰器和闭包

### 9.1 装饰器基础知识

装饰器的基本性质：

- 装饰器是一个函数或其他可调用对象。
- 装饰器可以把被装饰的函数替换成别的函数。
- 装饰器在加载（导入）模块时立即执行。

```python
def deco(func):
    def inner():
        print('running inner')
    return inner

@deco
def target():
    print('running target()')
>>>target()
running inner
>>>target
<function __main__.deco.<locals>.inner()>
```

### 9.2 闭包

闭包：延伸了作用域的函数，包括函数（f）主体中引用的非全局变量和局部变量。这些变量必须来自包含f的外部函数的局部作用域。

```python
# 一个计算累计平均值的高阶函数，所有值存储在历史数列series中
def make_averager():
    series = []
   
    def averager(new_value):
        series.append(new_value)
        total = sum(series)
        return total / len(series)
    
    return averager
>>>avg = make_averager()
>>>avg(10)
10.0
>>>avg(11)
10.5
>>>avg(15)
12.0
# avg的局部变量
>>>avg.__code__.co_varnames
('new_value', 'total')
>>># avg的自由变量
avg.__code__.co_freevars
('series',)
```

### 9.3 nonlocal声明

nonlocal：把变量标记为自由变量，便于在函数中为变量赋予新值。

```python
# 计算累计平均值，不保存所有历史
def make_averager():
    count = 0
    total = 0
    
    def averager(new_value):
        nonlocal count, total
        count += 1
        total += new_value
        return total / count
    
    return averager
```

### 9.4 变量查找逻辑

- 如果是`global x`声明，则`x`来自模块全局作用域，并赋予那个作用域中`x`的值。

- 如果是`nonlocal x`声明，则`x`来自最近一个定义它的外层函数，并赋予那个函数中局部变量`x`的值。

- 如果`x`是参数，或者在函数主体中赋了值，那么`x`就是局部变量。

- 如果引用了x，但是没有赋值也不是参数，则需要遵循以下规则：

  - 在外层函数主体的局部作用域（非局部作用域）内查找`x`。
  - 如果在外层作用域类没有找到，则从模块全局作用域内读取。
  - 如果在模块全局作用域内没有找到，则从`__builtins__.__dict__`中读取。

### 9.5 实现一个简单的装饰器

装饰器的主要作用是在每次调用被装饰的函数时计时，把运行时间、传入的参数和调用的结果打印出来。

```python
import time
import functools


def clock(func):
    @functools.wraps(func)		# 协助构建行为良好的装饰器
    def clocked(*args, **kwargs):
        t0 = time.perf_counter()
        # 调用被装饰的函数
        result = func(*args, **kwargs)
        elapsed = time.perf_counter() - t0
        name = func.__name__
        arg_lst = [repr(arg) for arg in args]
        arg_lst.extend(f'{k}={v!r}' for k, v in kwargs.items())
        arg_str = ', '.join(arg_lst)
        print(f'[{elapsed:0.8f}s] {name}({arg_str}) -> {result!r}')        
        return result
    return clocked
@clock
def snooze(seconds):
    time.sleep(seconds)
@clock
def factorial(n):
    return 1 if n < 2 else n*factorial(n-1)
if __name__ == '_main_':
	print('*' * 40, 'Calling snooze(.123)')
	snooze(.123)
	print('*' * 40, 'Calling factorial(6)')
	print('6! =', factorial(6))
>>>**************************************** Calling snooze(.123)
>>>[0.13659960s] snooze(0.123) -> None
>>>**************************************** Calling factorial(6)
>>>[0.00000060s] factorial(1) -> 1
>>>[0.00001260s] factorial(2) -> 2
>>>[0.00001960s] factorial(3) -> 6
>>>[0.00002570s] factorial(4) -> 24
>>>[0.00003420s] factorial(5) -> 120
>>>[0.00004170s] factorial(6) -> 720
>>>6! = 720
```

### 9.6 标准库中的装饰器

#### 9.6.1 使用`functools.cache`做备忘

`functools.cache`装饰器实现了备忘，能把耗时的函数得到的结果保存起来，避免传入相同的参数时重复计算。

```python
import functools

@functools.cache
@clock
def fibonacci(n):
    if n < 2:
        return n
    return fibonacci(n - 2) + fibonacci(n - 1)
if __name__ == '_main_':
	print(fibonacci(6))
>>>[0.00000070s] fibonacci(0) -> 0
>>>[0.00000040s] fibonacci(1) -> 1
>>>[0.00019480s] fibonacci(2) -> 1
>>>[0.00000050s] fibonacci(3) -> 2
>>>[0.00020520s] fibonacci(4) -> 3
>>>[0.00000040s] fibonacci(5) -> 5
>>>[0.00021450s] fibonacci(6) -> 8
>>>8
```

上述的叠放装饰器相当于`fibonacci = functools.cache(clock(fibonacci)`

#### 9.6.2 单分派泛化函数

`functools.singledispatch`装饰器可以把整体方案拆分成多个模块，甚至可以为第三方包中无法编辑的类型提供专门的函数，将普通函数变成了泛化函数的入口，即为单分派。如果根据多个参数选择专门的函数，则是多分派。

**需求：**

开发一个调试Web应用程序的工具，生成HTML，以显示不同类型的Python对象。需要满足如下功能：

1. 当参数为`str`时，内部的换行符替换为`<br/>\n`，不使用`<pre>`标签，使用`<p>`。
2. 当参数为`int`时，以十进制和十六进制显示数（bool除外）。
3. 当参数为`list`时，输出一个HTML列表，根据各项的类型进行格式化。
4. 当参数为`float`和`Decimal`时，正常输出值，外加分数形式。

```python
from functools import singledispatch
from collections import abc
import fractions
import decimal
import html
import numbers

@singledispatch
def htmlize(obj: object) -> str:
    content = html.escape(repr(obj))
    return f'<pre>{content}</pre>'

@htmlize.register
def _(text: str) -> str: 
    content = html.escape(text).replace('\n', '<br/>\n')
    return f'<p>{content}</p>'

@htmlize.register
def _(seq: abc.Sequence) -> str:
    inner = '</li>\n<li>'.join(htmlize(item) for item in seq)
    return '<ul>\n<li>' + inner + '</li>\n</ul>'

@htmlize.register
def _(n: numbers.Integral) -> str:
    return f'<pre>{n} (0x{n:x})</pre>'

@htmlize.register
def _(n: bool) -> str:
    return f'<pre>{n}</pre>'

@htmlize.register(fractions.Fraction)
def _(x) -> str:
    frac = fractions.Fraction(x)
    return f'<pre>{frac.numerator}/{frac.denominator}</pre>'

@htmlize.register(decimal.Decimal)
@htmlize.register(float)
def _(x) -> str:
    frac = fractions.Fraction(x).limit_denominator()
    return f'<pre>{x} ({frac.numerator}/{frac.denominator})</pre>'
>>>htmlize({1, 2, 3})
'<pre>{1, 2, 3}</pre>'
>>>htmlize(abs)
'<pre>&lt;built-in function abs&gt;</pre>'
>>>htmlize('Heimlich & Co.\n- a game')
'<p>Heimlich &amp; Co.<br/>\n- a game</p>'
>>>htmlize(42)
'<pre>42 (0x2a)</pre>'
>>>print(htmlize(['alpha', 66, {3, 2, 1}]))
<ul>
<li><p>alpha</p></li>
<li><pre>66 (0x42)</pre></li>
<li><pre>{1, 2, 3}</pre></li>
</ul>
>>>htmlize(True)
'<pre>True</pre>'
>>>htmlize(fractions.Fraction(2, 3))
'<pre>2/3</pre>'
>>>htmlize(2/3)
'<pre>0.6666666666666666 (2/3)</pre>'
>>>htmlize(decimal.Decimal('0.02380952'))
'<pre>0.02380952 (1/42)</pre>'
```

### 9.7 参数化装饰器

接收其他参数的装饰器：创建一个装饰器工厂函数来接收那些参数，然后再返回一个装饰器，应用到被装饰的函数上。

#### 9.7.1 参数化clock装饰器

```python
import time
DEFAULT_FMT = '[{elapsed:0.8f}s] {name}({args}) -> {result}'

def clock(fmt=DEFAULT_FMT): # clock是参数化装饰器的工厂函数
    def decorate(func):     # 真正的装饰器 
        def clocked(*_args):  # 包装被装饰的函数 
            t0 = time.perf_counter()
            _result = func(*_args)  # 调用被装饰的函数
            elapsed = time.perf_counter() - t0
            name = func.__name__
            args = ', '.join(repr(arg) for arg in _args) 
            result = repr(_result)  
            print(fmt.format(**locals()))
            return _result
        return clocked 
    return decorate
if __name__ == '__main__':
	@clock()
	def snooze(seconds):
    	time.sleep(seconds)

	for i in range(3):
    	snooze(.123)
>>>[0.13203000s] snooze(0.123) -> None
>>>[0.12454020s] snooze(0.123) -> None
>>>[0.12390610s] snooze(0.123) -> None
@clock('{name}: {elapsed}s')
def snooze(seconds):
    time.sleep(seconds)

for i in range(3):
    snooze(.123)
>>>snooze: 0.12821319999784464s
>>>snooze: 0.12511039999662898s
>>>snooze: 0.1259561000042595s
@clock('{name}({args}) dt={elapsed:0.3f}s')
def snooze(seconds):
    time.sleep(seconds)

for i in range(3):
    snooze(.123)
>>>snooze(0.123) dt=0.126s
>>>snooze(0.123) dt=0.124s
>>>snooze(0.123) dt=0.124s
```

#### 9.7.2 基于类的clock装饰器

```python
import time
DEFAULT_FMT = '[{elapsed:0.8f}s] {name}({args}) -> {result}'

class clock:

    def __init__(self, fmt=DEFAULT_FMT):  
        self.fmt = fmt

    def __call__(self, func):
        def clocked(*_args):
            t0 = time.perf_counter()
            _result = func(*_args)
            elapsed = time.perf_counter() - t0
            name = func.__name__
            args = ', '.join(repr(arg) for arg in _args)
            result = repr(_result)
            print(self.fmt.format(**locals()))
            return _result
        return clocked
```

## 第10章 使用一等函数实现设计模式

### 10.1 案例分析：重构策略模式

**典型示例：**

根据客户的属性或订单中的商品计算折扣，假如某个网店制定了以下折扣规则：

1. 有1000或以上积分的顾客，每个订单享5%折扣。
2. 同一个订单中，单个商品的数量达到20个或以上，享10%折扣。
3. 订单中不同商品的数量达到10个或以上，享7%折扣。

#### 10.1.1 典型策略模式

```python
from abc import ABC, abstractmethod
from collections.abc import Sequence
from decimal import Decimal
from typing import NamedTuple, Optional

class Customer(NamedTuple):
    name: str
    fidelity: int

class LineItem(NamedTuple):
    product: str
    quantity: int
    price: Decimal

    def total(self) -> Decimal:
        return self.price * self.quantity

class Order(NamedTuple):	# 上下文
    customer: Customer
    cart: Sequence[LineItem]
    promotion: Optional['Promotion'] = None

    def total(self) -> Decimal:
        totals = (item.total() for item in self.cart)
        return sum(totals, start=Decimal(0))

    def due(self) -> Decimal:
        if self.promotion is None:
            discount = Decimal(0)
        else:
            discount = self.promotion.discount(self)
        return self.total() - discount

    def __repr__(self):
        return f'<Order total: {self.total():.2f} due: {self.due():.2f}>'

class Promotion(ABC):	# 策略：抽象基类
    @abstractmethod
    def discount(self, order: Order) -> Decimal:
        """返回折扣金额（正值）"""

class FidelityPromo(Promotion):
    """第一个具体策略：为积分是1000或以上的顾客提供5%折扣。"""

    def discount(self, order: Order) -> Decimal:
        rate = Decimal('0.05')
        if order.customer.fidelity >= 1000:
            return order.total() * rate
        return Decimal(0)

class BulkItemPromo(Promotion):
    """第二个具体策略：单个商品的数量为20个或以上时，提供10%折扣。"""

    def discount(self, order: Order) -> Decimal:
        discount = Decimal(0)
        for item in order.cart:
            if item.quantity >= 20:
                discount += item.total() * Decimal('0.1')
        return discount

class LargeOrderPromo(Promotion):
    """第三个具体策略：订单中不同商品的数量达到10个或以上时，提供7%折扣。"""

    def discount(self, order: Order) -> Decimal:
        distinct_items = {item.product for item in order.cart}
        if len(distinct_items) >= 10:
            return order.total() * Decimal('0.07')
        return Decimal(0)
# Joe的积分为0
>>>joe = Customer('John Doe', 0)
# Ann的积分为1100
>>>ann = Customer('Ann Smith', 1100)
# 购物车中有3个商品
>>>cart = (LineItem('banana', 4, Decimal('.5')), 
...        LineItem('apple', 10, Decimal('1.5')),
...        LineItem('watermelon', 5, Decimal(5)))
# joe没有折扣
>>>Order(joe, cart, FidelityPromo())
<Order total: 42.00 due: 42.00>
# Ann得到了5%折扣
>>>Order(ann, cart, FidelityPromo())
<Order total: 42.00 due: 39.90>
# 有30个香蕉和10个苹果
>>>banana_cart = (LineItem('banana', 30, Decimal('.5')),
...               LineItem('apple', 10, Decimal('1.5')))
# joe购买时优惠了1.5美元
>>>Order(joe, banana_cart, BulkItemPromo())
<Order total: 30.00 due: 28.50>
# 有10个不同的商品
>>>long_cart = tuple(LineItem(str(sku), 1, Decimal(1)) 
                     for sku in range(10))
# 为joe提供了7%折扣
>>>Order(joe, long_cart, LargeOrderPromo()) 
<Order total: 10.00 due: 9.30>
```

#### 10.1.2 使用函数实现策略模式

把具体策略换成简单的函数，去掉抽象基类`Promotion`，Order类也修改了。

```python
from dataclasses import dataclass
from typing import Callable

@dataclass(frozen=True)
class Order:	# 上下文
    customer: Customer
    cart: Sequence[LineItem]
    # 可以接收一个Order参数，并返回一个Decimal值的可调用对象
    promotion: Optional[Callable[['Order'], Decimal]] = None

    def total(self) -> Decimal:
        totals = (item.total() for item in self.cart)
        return sum(totals, start=Decimal(0))

    def due(self) -> Decimal:
        if self.promotion is None:
            discount = Decimal(0)
        else:
            discount = self.promotion(self)
        return self.total() - discount

    def __repr__(self):
        return f'<Order total: {self.total():.2f} due: {self.due():.2f}>'

def fidelity_promo(order: Order) -> Decimal:
    """第一个具体策略：为积分是1000或以上的顾客提供5%折扣。"""
    if order.customer.fidelity >= 1000:
        return order.total() * Decimal('0.05')
    return Decimal(0)

def bulk_item_promo(order: Order) -> Decimal:
    """第二个具体策略：单个商品的数量为20个或以上时，提供10%折扣。"""
    discount = Decimal(0)
    for item in order.cart:
        if item.quantity >= 20:
            discount += item.total() * Decimal('0.1')
    return discount

def large_order_promo(order: Order) -> Decimal:
    """第三个具体策略：订单中不同商品的数量达到10个或以上时，提供7%折扣。"""
    distinct_items = {item.product for item in order.cart}
    if len(distinct_items) >= 10:
        return order.total() * Decimal('0.07')
    return Decimal(0)
```

#### 10.1.3 选择最佳策略的简单方式

方法：直接计算所有策略，选取折扣幅度最大的那一个

```python
promos = [fidelity_promo, bulk_item_promo, large_order_promo]

def best_promo(order: Order) -> Decimal:
    """选择可用的最佳折扣"""
    return max(promo(order) for promo in promos)
>>>Order(joe, long_cart, best_promo)
<Order total: 10.00 due: 9.30>
>>>Order(joe, banana_cart, best_promo)
<Order total: 30.00 due: 28.50>
>>>Order(ann, cart, best_promo)
<Order total: 42.00 due: 39.90>
```

#### 10.1.4 找出一个模块中的全部策略

方法1：使用`globals`函数，帮助`best_promo`自动找到其他可用的`*_promo`函数。

```python
promos = [promo for name, promo in globals().items()  
                if name.endswith('_promo') and        
                   name != 'best_promo'               
]

def best_promo(order: Order) -> Decimal:              
    """选择可用的最佳折扣"""
    return max(promo(order) for promo in promos)
```

方法2：使用`inspect.getmembers`函数获取对象的属性。

```python
import inspect
# 该模块包含所有的策略函数
import promotions

# 得到promotins模块下所有的函数对象
promos = [func for _, func in inspect.getmembers(promotions, inspect.isfunction)]

def best_promo(order: Order) -> Decimal:
    """选择可用的最佳折扣"""
    return max(promo(order) for promo in promos)
```

### 10.2 使用装饰器改进策略模式

```python
Promotion = Callable[[Order], Decimal]
promos: list[Promotion] = []

# 注册装饰器
def promotion(promo: Promotion) -> Promotion:	# Promotion是注册装饰器
    promos.append(promo)
    return promo

def best_promo(order: Order) -> Decimal:
    """选择可用的最佳折扣"""
    return max(promo(order) for promo in promos)  # <3>

@promotion
def fidelity(order: Order) -> Decimal:
    """第一个具体策略：为积分是1000或以上的顾客提供5%折扣。"""
    if order.customer.fidelity >= 1000:
        return order.total() * Decimal('0.05')
    return Decimal(0)

@promotion
def bulk_item(order: Order) -> Decimal:
    """第二个具体策略：单个商品的数量为20个或以上时，提供10%折扣。"""
    discount = Decimal(0)
    for item in order.cart:
        if item.quantity >= 20:
            discount += item.total() * Decimal('0.1')
    return discount

@promotion
def large_order(order: Order) -> Decimal:
    """第三个具体策略：订单中不同商品的数量达到10个或以上时，提供7%折扣。"""
    distinct_items = {item.product for item in order.cart}
    if len(distinct_items) >= 10:
        return order.total() * Decimal('0.07')
    return Decimal(0)
```

优点：

1. 促销策略函数无须使用特殊的名称（不用以`_promo`结尾）。
2. `@promotion`装饰器突出了被装饰的函数作用，还便于临时禁用某个促销策略。
3. 促销折扣策略可以在其他模块中定义。

## 第11章 符合Python风格的对象

### 11.1 对象字符串表示形式

- repr()：便于开发者理解的方式返回对象的字符串表示形式。支持方法是`__repr__`。
- str()：便于用户理解的方式返回对象的字符串表示形式，支持方法是`__str__`。
- bytes()：获取对象的字节序列表示形式，支持方法是`__bytes__`。
- format()和str.format()：以特殊的格式化代码显示对象的字符串表示形式，支持方法是`obj.__format__(format_spec)`。

### 11.2 向量类实现

**需求：**

1. Vector2d实例的分量可以直接通过属性访问（无需调用读值方法）。
2. Vector2d实例可以拆包成变量元组。
3. Vector2d实例的表示形式模拟源码构建的实例的形式。
4. 可以支持`==`比较。
5. 支持`bytes`函数，输出实例的二进制表示形式。
6. 支持`abs`函数，返回Vector2d实例的模。
7. 支持`bool`函数，如果Vector2d实例的模为零，就返回False，否则返回True。

```python
from array import array
import math

class Vector2d_v1:
    # 在Vector2d实例和字节序列之间转换时使用
    typecode = 'd'

    def __init__(self, x, y):
        self.x = float(x)   
        self.y = float(y)

    def __iter__(self):
        # 将实例变成可迭代对象
        return (i for i in (self.x, self.y))

    def __repr__(self):
        class_name = type(self).__name__
        # 使用!r获取各个分量的表示形式
        return '{}({!r}, {!r})'.format(class_name, *self) 

    def __str__(self):
        # 得到一个元组，显示为有序对
        return str(tuple(self))

    def __bytes__(self):
        return (bytes([ord(self.typecode)]) +  
                bytes(array(self.typecode, self)))  

    def __eq__(self, other):
        return tuple(self) == tuple(other)  

    def __abs__(self):
        # 计算x分量和y分量构成的直角三角形的斜边长
        return math.hypot(self.x, self.y)  

    def __bool__(self):
        return bool(abs(self)) 
    
    def angle(self):
        return math.atan2(self.y, self.x)		# 返回给定的 X 及 Y 坐标值的反正切值
    
    def __format__(self, fmt_spec=''):
        if fmt_spec.endswith('p'):
            # 如果以p结尾，使用极坐标
            fmt_spec = fmt_spec[:-1]
            # 构建元组表示极坐标
            coords = (abs(self), self.angle())
            outer_fmt = '<{}, {}>' 
        else:
            # 如果不以p结尾，使用x分量和y分量构建直角坐标
            coords = self 
            outer_fmt = '({}, {})'  
        components = (format(c, fmt_spec) for c in coords) 
        return outer_fmt.format(*components)
    
    @classmethod 
    def frombytes(cls, octets):
        # 从第一个字节中读取tpyecode
        typecode = chr(octets[0]) 
        # 创建一个memoryview，使用typecode进行转换
        memv = memoryview(octets[1:]).cast(typecode)
        # 得到构造函数所需的一对参数
        return cls(*memv)
    
>>>v1 = Vector2d_v1(3, 4)
>>>print(v1.x, v1.y)
3.0 4.0
>>>x, y = v1
>>>x, y
(3.0, 4.0)
>>>v1
Vector2d_v1(3.0, 4.0)
>>>v1_clone = eval(repr(v1))
>>>v1 == v1_clone
True
>>>octets = bytes(v1)
>>>octets
b'd\x00\x00\x00\x00\x00\x00\x08@\x00\x00\x00\x00\x00\x00\x10@'
>>>abs(v1)
5.0
>>>bool(v1), bool(Vector2d_v1(0, 0))
(True, False)
```

### 11.3 classmethod与staticmethod

- classmethod：定义操作类而不是操作实例的方法，常见用途是定义备选构造函数。
- staticmethod：静态方法，不是特别有用。

### 11.4 格式化显示

格式规范微语言为一些内置类型提供了专用的表示代码，`b`和`x`分别表示二进制和十六进制的`int`类型，`f`表示小数形式的`float`类型，`%`表示百分数形式。

```python
>>>format(Vector2d_v1(1, 1), 'p')
'<1.4142135623730951, 0.7853981633974483>'
>>>format(Vector2d_v1(1, 1), '.3ep')
'<1.414e+00, 7.854e-01>'
>>>format(Vector2d_v1(1, 1), '0.5fp')
'<1.41421, 0.78540>'
```

### 11.5 可哈希的Vector2d和支持位置模式匹配

```python
from array import array
import math

class Vector2d_v2:
    __match_args__ = ('x', 'y')

    typecode = 'd'

    def __init__(self, x, y):
        self.__x = float(x)
        self.__y = float(y)

    @property
    def x(self):
        return self.__x

    @property
    def y(self):
        return self.__y

    def __iter__(self):
        return (i for i in (self.x, self.y))

    def __repr__(self):
        class_name = type(self).__name__
        return '{}({!r}, {!r})'.format(class_name, *self)

    def __str__(self):
        return str(tuple(self))

    def __bytes__(self):
        return (bytes([ord(self.typecode)]) +
                bytes(array(self.typecode, self)))

    def __eq__(self, other):
        return tuple(self) == tuple(other)

    def __hash__(self):
        return hash((self.x, self.y))

    def __abs__(self):
        return math.hypot(self.x, self.y)

    def __bool__(self):
        return bool(abs(self))

    def angle(self):
        return math.atan2(self.y, self.x)

    def __format__(self, fmt_spec=''):
        if fmt_spec.endswith('p'):
            fmt_spec = fmt_spec[:-1]
            coords = (abs(self), self.angle())
            outer_fmt = '<{}, {}>'
        else:
            coords = self
            outer_fmt = '({}, {})'
        components = (format(c, fmt_spec) for c in coords)
        return outer_fmt.format(*components)

    @classmethod
    def frombytes(cls, octets):
        typecode = chr(octets[0])
        memv = memoryview(octets[1:]).cast(typecode)
        return cls(*memv)
# 支持可哈希
>>>v1 = Vector2d_v2(3, 4)
>>>v2 = Vector2d_v2(3.1, 4.2)
>>>hash(v1), hash(v2)
(1079245023883434373, 1994163070182233067)
>>>{v1, v2}
{Vector2d_v2(3.0, 4.0), Vector2d_v2(3.1, 4.2)}
```

### 11.6 Python私有属性和“受保护”的属性

- Python没有私有属性的保护机制，在前面加上两个前导下划线，尾部没有或最多有一个下划线，则会进行**名称改写**。
- 约定使用一个下划线前缀编写“受保护”的属性，Python解释器不会对使用单个下划线的属性名做特殊处理。

### 11.7 使用`__slots__`节省空间

```python
class Vector2d_v3(Vector2d_v2):
    # 位置模式匹配可用的公开属性名称
    __match_args__ = ('x', 'y')
    # 列出实例属性名称
    __slots__ = ('__x', '__y')

    typecode = 'd'

    def __init__(self, x, y):
        self.__x = float(x)
        self.__y = float(y)

    @property
    def x(self):
        return self.__x

    @property
    def y(self):
        return self.__y

    def __iter__(self):
        return (i for i in (self.x, self.y))

    def __repr__(self):
        class_name = type(self).__name__
        return '{}({!r}, {!r})'.format(class_name, *self)

    def __str__(self):
        return str(tuple(self))

    def __bytes__(self):
        return (bytes([ord(self.typecode)]) +
                bytes(array(self.typecode, self)))

    def __eq__(self, other):
        return tuple(self) == tuple(other)

    def __hash__(self):
        return hash((self.x, self.y))

    def __abs__(self):
        return math.hypot(self.x, self.y)

    def __bool__(self):
        return bool(abs(self))

    def angle(self):
        return math.atan2(self.y, self.x)

    def __format__(self, fmt_spec=''):
        if fmt_spec.endswith('p'):
            fmt_spec = fmt_spec[:-1]
            coords = (abs(self), self.angle())
            outer_fmt = '<{}, {}>'
        else:
            coords = self
            outer_fmt = '({}, {})'
        components = (format(c, fmt_spec) for c in coords)
        return outer_fmt.format(*components)

    @classmethod
    def frombytes(cls, octets):
        typecode = chr(octets[0])
        memv = memoryview(octets[1:]).cast(typecode)
        return cls(*memv)
>>>v1 = Vector2d_v3(1.1, 2.2)
>>>dumpd = bytes(v1)
>>>dumpd
b'd\x9a\x99\x99\x99\x99\x99\xf1?\x9a\x99\x99\x99\x99\x99\x01@'
>>>len(dumpd)
17
>>>v1.typecode = 'f'
>>>dumpf = bytes(v1)
>>>dumpf
b'f\xcd\xcc\x8c?\xcd\xcc\x0c@'
>>>len(dumpf)
9
```

## 第12章 序列的特殊方法

### 12.1 Vector类第1版：与Vector2d类兼容

```python
from array import array
import reprlib
import math


class VectorV1:
    typecode = 'd'

    def __init__(self, components):
        # 将Vector的分量保存在一个数组中
        self._components = array(self.typecode, components)

    def __iter__(self):
        return iter(self._components)

    def __repr__(self):
        # 生成有限长度表示形式
        components = reprlib.repr(self._components) 
        components = components[components.find('['):-1]
        return f'Vector({components})'

    def __str__(self):
        return str(tuple(self))

    def __bytes__(self):
        return (bytes([ord(self.typecode)]) +
                bytes(self._components))

    def __eq__(self, other):
        return tuple(self) == tuple(other)

    def __abs__(self):
        return math.hypot(*self)

    def __bool__(self):
        return bool(abs(self))

    @classmethod
    def frombytes(cls, octets):
        typecode = chr(octets[0])
        memv = memoryview(octets[1:]).cast(typecode)
        return cls(memv)
VectorV1([3.1, 4.2])
Vector([3.1, 4.2])
VectorV1((3, 4, 5))
Vector([3.0, 4.0, 5.0])
VectorV1(range(10))
Vector([0.0, 1.0, 2.0, 3.0, 4.0, ...])
```

### 12.2 Vector类第2版：可切片的序列

- 序列协议：任何类，只要使用标准的签名和语义实现了`__len__`和`__getitem__`方法，就能用在任何预期序列的地方。
- 协议是非正式的，没有强制力的，因此如果知道类的具体使用场景，通常只需要实现协议的一部分。

**改进方案：**

1. 新增`__len__`方法，计算Vector分量的个数。
2. 新增`__getitem__`方法，如果传入的参数是一个区间，则按照区间使用切片生成新的Vector，如果是单个索引，则返回相应的元素。

```python
import operator

class VectorV2:
    typecode = 'd'

    def __init__(self, components):
        # 将Vector的分量保存在一个数组中
        self._components = array(self.typecode, components)

    def __iter__(self):
        return iter(self._components)

    def __repr__(self):
        # 生成有限长度表示形式
        components = reprlib.repr(self._components) 
        components = components[components.find('['):-1]
        return f'Vector({components})'

    def __str__(self):
        return str(tuple(self))

    def __bytes__(self):
        return (bytes([ord(self.typecode)]) +
                bytes(self._components))

    def __eq__(self, other):
        return tuple(self) == tuple(other)

    def __abs__(self):
        return math.hypot(*self)

    def __bool__(self):
        return bool(abs(self))
    
    def __len__(self):
        return len(self._components)

    def __getitem__(self, key):
        if isinstance(key, slice):
            # 如果是一个区间，获取实例的类
            cls = type(self)  
            # 调用类的构造函数，使用切片构建一个新的Vector实例
            return cls(self._components[key])
        # 单个索引
        index = operator.index(key)
        # 返回相应的元素
        return self._components[index]  
    
    @classmethod
    def frombytes(cls, octets):
        typecode = chr(octets[0])
        memv = memoryview(octets[1:]).cast(typecode)
        return cls(memv)
v7 = VectorV2(range(7))
v7[-1]
6.0
v7[1:4]
Vector([1.0, 2.0, 3.0])
v7[-1:]
Vector([6.0])
```

### 12.3 Vector类第3版：动态存取属性

**改进方案：**

1. 新增支持位置模式匹配`__match_args__`。
2. 新增`__getattr__`方法：得到元素的相应位置，如果在范围内，则返回相应的元素。
3. 新增`__setattr__`方法：如果参数是受特性保护的只读属性，则抛出异常，如果是小写字母，则抛出错误警告。

```python
class VectorV3:
    typecode = 'd'

    def __init__(self, components):
        self._components = array(self.typecode, components)

    def __iter__(self):
        return iter(self._components)

    def __repr__(self):
        components = reprlib.repr(self._components)
        components = components[components.find('['):-1]
        return f'Vector({components})'

    def __str__(self):
        return str(tuple(self))

    def __bytes__(self):
        return (bytes([ord(self.typecode)]) +
                bytes(self._components))

    def __eq__(self, other):
        return tuple(self) == tuple(other)

    def __abs__(self):
        return math.hypot(*self)

    def __bool__(self):
        return bool(abs(self))

    def __len__(self):
        return len(self._components)

    def __getitem__(self, key):
        if isinstance(key, slice):
            cls = type(self)
            return cls(self._components[key])
        index = operator.index(key)
        return self._components[index]
    
    # 支持位置模式匹配
    __match_args__ = ('x', 'y', 'z', 't')  

    def __getattr__(self, name):
        # 获取Vector类型
        cls = type(self)  
        try:
            # 得到位置
            pos = cls.__match_args__.index(name)  
        except ValueError: 
            pos = -1
        if 0 <= pos < len(self._components):
            # 如果位置处于范围类，则返回对应的分量
            return self._components[pos]
        msg = f'{cls.__name__!r} object has no attribute {name!r}'
        raise AttributeError(msg)
        
    def __setattr__(self, name, value):
        cls = type(self)
        if len(name) == 1:
            # 处理名称是单个字符的属性
            if name in cls.__match_args__:
                # 受特性保护的只读属性
                error = 'readonly attribute {attr_name!r}'
            elif name.islower():
                error = "can't set attributes 'a' to 'z' in {cls_name!r}"
            else:
                error = ''
            if error:
                msg = error.format(cls_name=cls.__name__, attr_name=name)
                raise AttributeError(msg)
        # 调用超类的setattr方法        
        super().__setattr__(name, value)    
v = VectorV3(range(10))
v.x
0.0
v.y, v.z, v.t
(1.0, 2.0, 3.0)
```

### 12.4 Vector类第4版：哈希和快速等值测试

**改进方案：**

1. 新增`__eq__`方法：先判断两个对象的长度是否相等，再比较其中各个元素是否相等。
2. 新增`__hash__`方法：计算各个分量的哈希值，并使用`xor`运算符聚合所有的哈希值。

```python
class VectorV4:
    typecode = 'd'

    def __init__(self, components):
        self._components = array(self.typecode, components)

    def __iter__(self):
        return iter(self._components)

    def __repr__(self):
        components = reprlib.repr(self._components)
        components = components[components.find('['):-1]
        return f'Vector({components})'

    def __str__(self):
        return str(tuple(self))

    def __bytes__(self):
        return (bytes([ord(self.typecode)]) +
                bytes(self._components))

    def __eq__(self, other):
        # 先判断两个对象的长度是否相等
        # 再比较其中各个元素是否相等
        return (len(self) == len(other) and
                all(a == b for a, b in zip(self, other)))

    def __hash__(self):
        # 计算多个分量的哈希值
        hashes = (hash(x) for x in self)
        # v[0]^v[1]^v[2]^...
        # 使用xor运算符聚合所有的哈希值
        return functools.reduce(operator.xor, hashes, 0)

    def __abs__(self):
        return math.hypot(*self)

    def __bool__(self):
        return bool(abs(self))

    def __len__(self):
        return len(self._components)

    def __getitem__(self, key):
        if isinstance(key, slice):
            cls = type(self)
            return cls(self._components[key])
        index = operator.index(key)
        return self._components[index]

    __match_args__ = ('x', 'y', 'z', 't')

    def __getattr__(self, name):
        cls = type(self)
        try:
            pos = cls.__match_args__.index(name)
        except ValueError:
            pos = -1
        if 0 <= pos < len(self._components):
            return self._components[pos]
        msg = f'{cls.__name__!r} object has no attribute {name!r}'
        raise AttributeError(msg)

    @classmethod
    def frombytes(cls, octets):
        typecode = chr(octets[0])
        memv = memoryview(octets[1:]).cast(typecode)
        return cls(memv)
```

### 12.5 Vector第5版：格式化

**改进方案：**

1. 新增`angle(self, n)`函数：使用n维球体的公式计算角坐标。
2. 新增`angles`函数：创建生成器表达式，按需计算所有角坐标。
3. 新增`__format__`函数：根据球坐标标识符`h`，显示球面坐标。

```python
import itertools

class VectorV5:
    typecode = 'd'

    def __init__(self, components):
        self._components = array(self.typecode, components)

    def __iter__(self):
        return iter(self._components)

    def __repr__(self):
        components = reprlib.repr(self._components)
        components = components[components.find('['):-1]
        return f'Vector({components})'

    def __str__(self):
        return str(tuple(self))

    def __bytes__(self):
        return (bytes([ord(self.typecode)]) +
                bytes(self._components))

    def __eq__(self, other):
        return (len(self) == len(other) and
                all(a == b for a, b in zip(self, other)))

    def __hash__(self):
        hashes = (hash(x) for x in self)
        return functools.reduce(operator.xor, hashes, 0)

    def __abs__(self):
        return math.hypot(*self)

    def __bool__(self):
        return bool(abs(self))

    def __len__(self):
        return len(self._components)

    def __getitem__(self, key):
        if isinstance(key, slice):
            cls = type(self)
            return cls(self._components[key])
        index = operator.index(key)
        return self._components[index]

    __match_args__ = ('x', 'y', 'z', 't')

    def __getattr__(self, name):
        cls = type(self)
        try:
            pos = cls.__match_args__.index(name)
        except ValueError:
            pos = -1
        if 0 <= pos < len(self._components):
            return self._components[pos]
        msg = f'{cls.__name__!r} object has no attribute {name!r}'
        raise AttributeError(msg)

    def angle(self, n):
        # 使用n维球体的公式计算角坐标
        r = math.hypot(*self[n:])
        a = math.atan2(r, self[n-1])
        if (n == len(self) - 1) and (self[-1] < 0):
            return math.pi * 2 - a
        else:
            return a

    def angles(self):
        return (self.angle(n) for n in range(1, len(self)))

    def __format__(self, fmt_spec=''):
        if fmt_spec.endswith('h'):
            # 球坐标标识符h
            fmt_spec = fmt_spec[:-1]
            # 生成器表达式，迭代向量的模和各个角坐标
            coords = itertools.chain([abs(self)], self.angles())  
            # 显示球面坐标
            outer_fmt = '<{}>'  
        else:
            coords = self
            # 显示笛卡尔坐标
            outer_fmt = '({})' 
        components = (format(c, fmt_spec) for c in coords)  
        return outer_fmt.format(', '.join(components))  

    @classmethod
    def frombytes(cls, octets):
        typecode = chr(octets[0])
        memv = memoryview(octets[1:]).cast(typecode)
        return cls(memv)
```

## 第13章 接口、协议和抽象基类

- 鸭子类型：无需使用`isinstance`检查。
- 大鹅类型：Python>=2.6，使用`isinstance`检查是否符合抽象基类的要求。
- 静态类型：Python>=3.5，依靠PEP484实现的类型提示和外部类型检查工具。
- 静态鸭子类型：Python>=3.8，依靠PEP544实现的`typing.Protocol`类型提示和外部类型检查工具。

### 13.1 动态协议和静态协议

**定义：**

- 动态协议：Python大多数重要的动态协议由解释器支持。
- 静态协议：使用`typing.Protocol`子类显式定义。

**区别：**

- 对象可以只实现动态协议的一部分，如果想满足静态协议，则对象必须提供协议类中声明的每一个方法，即使程序用不到。
- 静态协议可以使用静态类型检查工具确认，动态协议则不能。

### 13.2 利用鸭子类型编程

#### 13.2.1 猴子补丁

```python
import collections

Card = collections.namedtuple('Card', ['rank', 'suit'])

class FrenchDeck:
    ranks = [str(n) for n in range(2, 11)] + list('JQKA')
    suits = 'spades diamonds clubs hearts'.split()

    def __init__(self):
        self._cards = [Card(rank, suit) for suit in self.suits
                                        for rank in self.ranks]

    def __len__(self):
        return len(self._cards)

    def __getitem__(self, position):
        return self._cards[position]
```

猴子补丁：在运行时动态修改模块、类或函数，以增加功能或修正bug。

```python
def set_card(deck, position, card):
    deck._cards[position] = card

# 打猴子补丁，把它变成可变序列
FrenchDeck.__setitem__ = set_card
from random import shuffle

deck = FrenchDeck()

shuffle(deck)
deck[:5]
[Card(rank='5', suit='clubs'),
 Card(rank='A', suit='diamonds'),
 Card(rank='3', suit='spades'),
 Card(rank='4', suit='clubs'),
 Card(rank='Q', suit='spades')]
```

以上代码，强调了猴子补丁，在运行时修改类或模块，而不改动源码，打补丁的代码与被打补丁的程序耦合十分紧密，而且往往要处理文档没有明确说明的私有属性。

#### 13.2.2 防御性编程和“快速失败”

- 如果一个函数接收一系列项，在内部按照列表处理，可以立即利用参数构造一个列表。

```python
def __init__(self, iterable):
    self._balls = list(iterable)Copy to clipboardErrorCopied
```

- 如果数据太多，需要就地修改数据，则应该使用`isinstance(x, abc.MutableSequence)`。
- 如果担心传入的是无穷生成器，则可以先使用`len()`获取参数的长度，遇到无效参数会立即抛出错误。

### 13.3 大鹅类型

大鹅类型的要求：

- 定义抽象基类的子类，明确表明在实现既有的接口。
- 运行时检查类型时，`isinstance`和`issubclass`的第二个参数要使用抽象基类，而不是具体类。

#### 13.3.1 子类化一个抽象基类

```python
from collections import namedtuple, abc

Card = namedtuple('Card', ['rank', 'suit'])

class FrenchDeck2(abc.MutableSequence):
    ranks = [str(n) for n in range(2, 11)] + list('JQKA')
    suits = 'spades diamonds clubs hearts'.split()

    def __init__(self):
        self._cards = [Card(rank, suit) for suit in self.suits
                                        for rank in self.ranks]

    def __len__(self):
        return len(self._cards)

    def __getitem__(self, position):
        return self._cards[position]

    def __setitem__(self, position, value):
        self._cards[position] = value

    def __delitem__(self, position):
        del self._cards[position]

    def insert(self, position, value):
        self._cards.insert(position, value)
```

**改进方案：**

1. 新增`__setitem__`方法，支持洗牌操作。
2. 继承了`MutableSequence`类，还需新增`__delitem__`方法和`insert`方法。

#### 13.3.2 定义并使用一个抽象基类

```python
import abc

class Tombola(abc.ABC):

    @abc.abstractmethod
    def load(self, iterable):         
        """从可迭代对象中添加元素"""

    @abc.abstractmethod
    def pick(self):  # <3>
        """随机删除元素，再返回被删除的元素。
        
        如果实例为空，那么这个方法应该抛出LookupError
        """

    def loaded(self):
        """如果至少有一个元素，就返回True，否则返回False"""
        return bool(self.inspect())

    def inspect(self):
        """返回由容器中的当前元素构成的有序元组"""
        items = []
        while True:
            try:
                items.append(self.pick())
            except LookupError:
                break
        self.load(items)  
        return tuple(items)
```

#### 13.3.3 子类化抽象基类Tombola

```python
import random

class BingoCage(Tombola):

    def __init__(self, items):
        # 使用随机发生器
        self._randomizer = random.SystemRandom()
        self._items = []
        # 实现初始加载
        self.load(items)

    def load(self, items):
        self._items.extend(items)
        # 使用随机发生器打乱序列
        self._randomizer.shuffle(self._items)

    def pick(self):
        try:
            return self._items.pop()
        except IndexError:
            raise LookupError('pick from empty BingoCage')

    def __call__(self):
        self.pick()
```

上述代码的`load`方法很耗时和`inspect`方法很笨拙，都可以覆盖调，以下代码进行了优化。

```python
class LottoBlower(Tombola):

    def __init__(self, iterable):
        self._balls = list(iterable)

    def load(self, iterable):
        self._balls.extend(iterable)

    def pick(self):
        try:
            position = random.randrange(len(self._balls))
        except ValueError:
            raise LookupError('pick from empty LottoBlower')
        # 取出一个随机位置上的球
        return self._balls.pop(position)

    def loaded(self):
        return bool(self._balls)

    def inspect(self):
        return tuple(self._balls)
```

#### 13.3.4 抽象基类的虚拟子类

大鹅类型的重要特性：

- 使用`register`的装饰器，将一个类注册为抽象基类的虚拟子类。
- 注册的类变成抽象基类的虚拟子类，而且`issubclass`函数能够识别这种关系，但是注册的类不会从抽象基类中集成任何方法或属性。

```python
from random import randrange

@Tombola.register
class TomboList(list):  

    def pick(self):
        if self:  
            # 获得随机的元素索引
            position = randrange(len(self))
            return self.pop(position)  
        else:
            raise LookupError('pop from empty TomboList')

    load = list.extend  

    def loaded(self):
        return bool(self)  

    def inspect(self):
        return tuple(self)
Tombola.register(TomboList)
__main__.TomboList
issubclass(TomboList, Tombola)
True
t = TomboList(range(100))
isinstance(t, Tombola)
True
# 类的继承关系
TomboList.__mro__
(__main__.TomboList, list, object)
```

### 13.4 静态协议

#### 13.4.1 为double函数添加类型提示

```python
from typing import TypeVar, Protocol

# 定义泛型
T = TypeVar('T')

class Repeatable(Protocol):
    def __mul__(self: T, repeat_count: int) -> T: ...  

RT = TypeVar('RT', bound=Repeatable)

def double(x: RT) -> RT:
    return x * 2
```

#### 13.4.2 设计一个静态协议

**运行时协议检查的局限性：**`isinstance`或`issubclass`只检查有没有特定的方法，不检查方法的签名，更不会检查方法的类型注解。

```python
from typing import runtime_checkable, Any

@runtime_checkable
class RandomPicker(Protocol):
    def pick(self) -> Any: ...
from typing import Iterable

class SimplePicker:
    def __init__(self, items: Iterable) -> None:
        self._items = list(items)
        random.shuffle(self._items)

    def pick(self) -> Any:
        return self._items.pop()
# 类型是相容的
popper: RandomPicker = SimplePicker([1])
assert isinstance(popper, RandomPicker)
```

#### 13.4.3 协议设计约定

- 使用朴素的名称命名协议，清楚表明概念。
- 使用SupportsX形式命名提供可调用方法的协议。
- 使用HasX形式命名有可读属性和可写属性，或者有读值方法和设值方法的协议。

## 第14章 继承：瑕瑜互见

### 14.1 super()函数

- 坚持使用内置函数`super()`是确保面向对象的Python程序可维护性的基本要求。
- super提供两个参数：
  - type：从哪里开始搜索实现所需方法的超类。默认为`super()`调用所在的方法所属的类。
  - object_or_type：接收方法调用的对象（调用实例方法时）或类（调用类方法时）。在实例方法中调用`super()`时，默认为`self`。

### 14.2 子类化内置类型

内置类型（使用C语言编写）通常不调用用户定义的类覆盖的方法。

```python
class DoppleDict(dict):
    def __setitem__(self, key, value):
        super().__setitem__(key, [value] * 2)
# dict的__init__方法忽略了覆盖的__setitem__方法
dd = DoppleDict(one=1)
dd
{'one': 1}
dd['two'] = 2
dd
{'one': 1, 'two': [2, 2]}
# update方法忽略了覆盖的__setitem__方法
dd.update(three=3)
dd
{'one': 1, 'two': [2, 2], 'three': 3}
```

### 14.3 多重继承和方法解析顺序

```python
class Root:
    def ping(self):
        print(f'{self}.ping() in Root')

    def pong(self):
        print(f'{self}.pong() in Root')

    def __repr__(self):
        cls_name = type(self).__name__
        return f'<instance of {cls_name}>'


class A(Root):  
    def ping(self):
        print(f'{self}.ping() in A')
        super().ping()

    def pong(self):
        print(f'{self}.pong() in A')
        super().pong()


class B(Root):  
    def ping(self):
        print(f'{self}.ping() in B')
        super().ping()

    def pong(self):
        print(f'{self}.pong() in B')


class Leaf(A, B):  
    def ping(self):
        print(f'{self}.ping() in Leaf')
        super().ping()
leaf1 = Leaf()
leaf1.ping()
<instance of Leaf>.ping() in Leaf
<instance of Leaf>.ping() in A
<instance of Leaf>.ping() in B
<instance of Leaf>.ping() in Root
leaf1.pong()
<instance of Leaf>.pong() in A
<instance of Leaf>.pong() in B
```

唤醒过程由以下两个因素决定：

- Leaf类的方法解析顺序。
- 各方法中使用的`super()`。

### 14.4 多重继承的实际运用

1. ThreadingMixIn和ForkingMixIn

`ThreadingHTTPServer`多重继承了`socketserver.ThreadingMixIn`类和`HTTPServer`类，其中：

- `process_request_thread`方法没有调用`super()`。
- `process_request`方法：属于覆盖方法，启动一个线程，并把具体工作委托给运行在该线程中的`process_request_thread`，没有调用`super()`。
- `server_close`调用了`super().server_close()`以停止接收请求，然后等待`process_request`启动的线程完成工作。

1. Django泛化视图混入类

- `View`是所有视图的基类，提供了核心功能，例如`dispatch`方法。
- `TemplateView`类仅用于显示内容。
- `TemplateResponseMixin`类只适用于需要使用模板的视图，为`TemplateView`和其他渲染模板的视图提供行为。
- `ListView`是一个聚合类，实例化后，模板通过迭代`object_list`属性显示页面内容。

1. Tkinter中的多重继承

- Toplevel：表示`Tkinter`应用程序中顶层窗口的类。所有图形类中唯一没有继承`Widget`。
- Widget：窗口中所有可见对象的超类。直接继承自`BaseWidget`，并继承了`Pack`、`Place`和`Grid`（几何管理器，负责在窗口或窗体中排布小组件）。
- Button：普通的按钮小组件。只是`Widget`的子代，也间接继承`Misc`。
- Entry：单行可编辑文本字段。是`Widget`和`XView`（支持横向滚动）的子类。
- Text：多行可编辑文本字段。是`Widget`、`XView`和`YView`（支持纵向滚动）的子类。

### 14.5 应对多重继承

- 优先使用对象组合，而不是类继承。
- 理解不同情况下使用继承的原因：
  - 继承接口，创建子类型，实现“是什么”关系。
  - 继承实现，通过重用避免代码重复。
- 使用抽象基类显式表示接口。
  - 如果类的作用式定义接口，则显示地定义为抽象基类或者`typing.Protocol`的子类。
  - 抽象基类只能子类化`abc.ABC`或其他抽象基类。
- 通过混入明确重用代码。如果一个类的作用是提供方法，以供多个不相关的子类重用，但不体现“是什么”关系，那么就应该把那个类明确地定义为混入类。
- 为用户提供聚合类。
- 仅子类化为子类化设计的类。*子类化复杂的类并覆盖类方法容易出错，因为超类中的方法可能在不知不觉中忽略子类覆盖的行为*。
- 避免子类化具体类。具体类的实例通常有内部状态，覆盖依赖内部状态的方法时，很容易破坏状态。

## 第15章 类型提示进阶

### 15.1 重载的签名

@typing.overload装饰器用于函数的重载。

```python
import functools
import operator
from collections.abc import Iterable
from typing import overload, Union, TypeVar

T = TypeVar('T')
S = TypeVar('S')  # <1>

@overload
def sum(it: Iterable[T]) -> Union[T, int]: ...  # <2>
@overload
def sum(it: Iterable[T], /, start: S) -> Union[T, S]: ...  # <3>
def sum(it, /, start=0):  # <4>
    return functools.reduce(operator.add, it, start)
```

其中：

- 省略号（...）没有特殊作用，只是为了满足句法的要求，类似于pass。
- 参数`/`用于分隔不同类型的参数，比如位置参数和关键字参数。

### 15.2 TypedDict

处理动态数据结构时，容易误用TypedDict来避免错误。

TypedDict的作用：

- 使用与类相似的句法注解字典，为各个“字段”的值提供类型提示。
- 通过一个构造函数告诉类型检查工具，字典应具有指定的键和指定类型的值。

```python
from typing import TypedDict, List
import json

class BookDict(TypedDict):
    isbn: str
    title: str
    authors: List[str]
    pagecount: int
AUTHOR_ELEMENT = '<AUTHOR>{}</AUTHOR>'

def to_xml(book: BookDict) -> str:
    elements: List[str] = []  
    for key, value in book.items():
        if isinstance(value, list):  
            elements.extend(AUTHOR_ELEMENT.format(n)
                for n in value)
        else:
            tag = key.upper()
            elements.append(f'<{tag}>{value}</{tag}>')
    xml = '\n\t'.join(elements)
    return f'<BOOK>\n\t{xml}\n</BOOK>'
def from_json(data: str) -> BookDict:
    whatever = json.loads(data)
    return whatever
print(to_xml({
        'isbn': '0134757599',
        'title': 'Refactoring, 2e',
        'authors': ['Martin Fowler', 'Kent Beck'],
        'pagecount': 478,
    }))
<BOOK>
    <ISBN>0134757599</ISBN>
    <TITLE>Refactoring, 2e</TITLE>
    <AUTHOR>Martin Fowler</AUTHOR>
    <AUTHOR>Kent Beck</AUTHOR>
    <PAGECOUNT>478</PAGECOUNT>
</BOOK>
```

### 15.3 类型校正

typing.cast可用于处理不受控制的代码中存在的类型检查问题或不正确的类型提示。

```python
from typing import cast

def find_first_str(a: list[object]) -> str:
    index = next(i for i, x in enumerate(a) if isinstance(x, str))
    # 至少有一个字符串才能执行到这里
    return cast(str, a[index])
```

### 15.4 在运行时读取类型提示

类型提示使用量增加会引起两个问题：

- 如果类型提示很多，导入模块使用的CPU和内存会更多。
- 引用尚未定义的类型需要使用字符串，而不是真正的类型。

问题解决方案：

- 不要直接读取`__annotations__`属性，使用`inspect.get_annotations`或`typing.get_type_hints`。
- 自己编写一个函数，简单包装`inspect.get_annotations`或`typing.get_type_hints`。在基准代码中调用自定义的函数，当行为有变时，只需修改一个函数即可。

### 15.5 实现一个泛化类

```python
import abc

class Tombola(abc.ABC):

    @abc.abstractmethod
    def load(self, iterable):         
        """从可迭代对象中添加元素"""

    @abc.abstractmethod
    def pick(self):  # <3>
        """随机删除元素，再返回被删除的元素。
        
        如果实例为空，那么这个方法应该抛出LookupError
        """

    def loaded(self):
        """如果至少有一个元素，就返回True，否则返回False"""
        return bool(self.inspect())

    def inspect(self):
        """返回由容器中的当前元素构成的有序元组"""
        items = []
        while True:
            try:
                items.append(self.pick())
            except LookupError:
                break
        self.load(items)  
        return tuple(items)
import random

from collections.abc import Iterable
from typing import TypeVar, Generic

T = TypeVar('T')

class LottoBlower(Tombola, Generic[T]):

    def __init__(self, items: Iterable[T]) -> None: 
        self._balls = list[T](items)

    def load(self, items: Iterable[T]) -> None:  
        self._balls.extend(items)

    def pick(self) -> T:  
        try:
            position = random.randrange(len(self._balls))
        except ValueError:
            raise LookupError('pick from empty LottoBlower')
        return self._balls.pop(position)

    def loaded(self) -> bool:  
        return bool(self._balls)

    def inspect(self) -> tuple[T, ...]:  
        return tuple(self._balls)
machine = LottoBlower[int](range(1, 11))
first = machine.pick()
remain = machine.inspect()

first, remain
(3, (1, 2, 4, 5, 6, 7, 8, 9, 10))
```

**泛型基本术语：**

- 泛型：具有一个或多个类型变量的类型。例如：`LottoBlower[T]`。
- 形式类型参数：泛型声明中出现的类型变量。例如：`abc.Mapping[KT, VT]`中的`KT`和`VT`。
- 参数化类型：使用具体类型参数声明的类型。例如：`LottoBlower[int]`和`abc.Mapping[str, float]`。
- 具体类型参数：声明参数化类型时，为参数提供的具体类型。例如：`LottoBlower[int]`中的`int`。

### 15.6 型变

#### 15.6.1 协变

```python
from typing import TypeVar, Generic


class Beverage:
    """任何饮料"""


class Juice(Beverage):
    """任何果汁"""


class OrangeJuice(Juice):
    """使用巴西橙子制作的美味果汁"""


# 设置covariant=True，表示协变的类型参数
T_co = TypeVar('T_co', covariant=True)  


class BeverageDispenser(Generic[T_co]):  
    def __init__(self, beverage: T_co) -> None:
        self.beverage = beverage

    def dispense(self) -> T_co:
        return self.beverage

def install(dispenser: BeverageDispenser[Juice]) -> None: 
    """安装一个果汁自动售货机"""Copy to clipboardErrorCopied
orange_juice_dispenser = BeverageDispenser(OrangeJuice())
install(orange_juice_dispenser)
```

#### 15.6.2 逆变

```python
from typing import TypeVar, Generic

class Refuse:
    """任何废弃物"""

class Biodegradable(Refuse):
    """可生物降解的废弃物"""

class Compostable(Biodegradable):
    """可制成肥料的废弃物"""

T_contra = TypeVar('T_contra', contravariant=True)  # <2>

class TrashCan(Generic[T_contra]):  # <3>
    def put(self, refuse: T_contra) -> None:
        """在倾倒之前存放垃圾"""

def deploy(trash_can: TrashCan[Biodegradable]):
    """放置一个垃圾桶，存放可生物降解的废弃物"""
bio_can: TrashCan[Biodegradable] = TrashCan()
deploy(bio_can)
trash_can: TrashCan[Refuse] = TrashCan()
deploy(trash_can)
```

#### 15.6.3 型变总结

- 不变类型：如果一个形式类型参数既出现在方法参数的类型提示中，又出现在方法的返回类型中，那么该参数必须是不可变的。

给定两个类型A和B，B与A相容，而且均不是`Any`

- `A:>B`：A是B的超类，或者A与B类型相同。
- `A<:B`：B是A的子类，或者A与B类型相同。
- 协变类型：对于`A:>B`，当满足`C[A] :> C[B]`时，泛型`C`是可协变的。
- 逆变类型：对于`A:>B`，当满足`K[A] <: K[B]`是，泛型`K`是可逆变的。

**型变经验法则：**

- 如果一个形式类型参数定义的是从对象中获取的数据类型，那么该形式类型参数可能是协变的。
- 如果一个形式类型参数定义的是对象初始化之后，向对象输入的数据类型，那么该形式类型参数可能是逆变的。
- 如果一个形式类型参数定义的是从对象中获取的数据类型，同时也是向对象输入的数据类型，那么该形式类型参数必定是不可变的。
- 形式参数类型最好是不变的。

### 15.7 实现泛化静态协议

```python
import math
from typing import NamedTuple, SupportsAbs

class Vector2d(NamedTuple):
    x: float
    y: float

    def __abs__(self) -> float:  # 让Vector2d与SupportsAbs相容
        return math.hypot(self.x, self.y)

def is_unit(v: SupportsAbs[float]) -> bool: 
    """v的模接近1时为True"""
    return math.isclose(abs(v), 1.0)
v0 = Vector2d(0, 1)
sqrt2 = math.sqrt(2)
v1 = Vector2d(sqrt2 / 2, sqrt2 / 2)
v2 = Vector2d(1, 1)
v3 = complex(.5, math.sqrt(3) / 2)
v4 = 1

assert is_unit(v0)
assert is_unit(v1)
assert not is_unit(v2)
assert is_unit(v3)
assert is_unit(v4)
```

## 第16章 运算符重载

对运算符重载的限制：

- 不能改变内置类型的运算符表达的意思。
- 不能新建运算符，只能重载现有运算符。
- 有些运算符不能重载：`is`、`and`、`or`和`not`。

### 16.1 一元运算符

- 一元取反算术运算符（`-`）：由`__neg__`实现。
- 一元取正算术运算符（`+`）：由`__pos__`实现。
- 按位否定（取反）整数（`~`）：由`__invert__`实现。

```python
from array import array
import reprlib
import math
import functools
import operator
import itertools


class VectorV6:
    typecode = 'd'

    def __init__(self, components):
        self._components = array(self.typecode, components)

    def __iter__(self):
        return iter(self._components)

    def __repr__(self):
        components = reprlib.repr(self._components)
        components = components[components.find('['):-1]
        return f'Vector({components})'

    def __str__(self):
        return str(tuple(self))

    def __bytes__(self):
        return (bytes([ord(self.typecode)]) +
                bytes(self._components))

    def __eq__(self, other):
        return (len(self) == len(other) and
                all(a == b for a, b in zip(self, other)))

    def __hash__(self):
        hashes = (hash(x) for x in self)
        return functools.reduce(operator.xor, hashes, 0)

    def __abs__(self):
        return math.hypot(*self)

    def __neg__(self):
        # 每个分量取反
        return self.__class__(-x for x in self)

    def __pos__(self):
        # 每个分量保持不变
        return self.__class__(self)

    def __bool__(self):
        return bool(abs(self))

    def __len__(self):
        return len(self._components)

    def __getitem__(self, key):
        if isinstance(key, slice):
            cls = type(self)
            return cls(self._components[key])
        index = operator.index(key)
        return self._components[index]

    __match_args__ = ('x', 'y', 'z', 't')

    def __getattr__(self, name):
        cls = type(self)
        try:
            pos = cls.__match_args__.index(name)
        except ValueError:
            pos = -1
        if 0 <= pos < len(self._components):
            return self._components[pos]
        msg = f'{cls.__name__!r} object has no attribute {name!r}'
        raise AttributeError(msg)

    def angle(self, n):
        r = math.hypot(*self[n:])
        a = math.atan2(r, self[n-1])
        if (n == len(self) - 1) and (self[-1] < 0):
            return math.pi * 2 - a
        else:
            return a

    def angles(self):
        return (self.angle(n) for n in range(1, len(self)))

    def __format__(self, fmt_spec=''):
        if fmt_spec.endswith('h'):  # hyperspherical coordinates
            fmt_spec = fmt_spec[:-1]
            coords = itertools.chain([abs(self)],
                                     self.angles())
            outer_fmt = '<{}>'
        else:
            coords = self
            outer_fmt = '({})'
        components = (format(c, fmt_spec) for c in coords)
        return outer_fmt.format(', '.join(components))

    @classmethod
    def frombytes(cls, octets):
        typecode = chr(octets[0])
        memv = memoryview(octets[1:]).cast(typecode)
        return cls(memv)

    def __add__(self, other):
        # 重载加法运算符
        try:
            # 生成(a,b)形式的元组
            pairs = itertools.zip_longest(self, other, fillvalue=0.0)
            return self.__class__(a + b for a, b in pairs)
        except TypeError:
            return NotImplemented

    def __radd__(self, other):
        return self + other
v1 = VectorV6([3, 4, 5])
v1 + (10, 20, 30)
Vector([13.0, 24.0, 35.0])
```

如果中缀运算符方法抛出异常，那么它将终止运算符分派机制。

### 16.2 重载标量乘法运算符（`*`）和点乘运算符（`@`）

```python
from collections import abc

class VectorV7(VectorV6):
    def __mul__(self, scalar):
        try:
            factor = float(scalar)
        except TypeError:
            return NotImplemented
        return self.__class__(n * factor for n in self)

    def __rmul__(self, scalar):
        return self * scalar

    def __matmul__(self, other):
        if (isinstance(other, abc.Sized) and
            isinstance(other, abc.Iterable)):
            if len(self) == len(other):
                return sum(a * b for a, b in zip(self, other))
            else:
                raise ValueError('@ requires vectors of equal length.')
        else:
            return NotImplemented

    def __rmatmul__(self, other):
        return self @ other
>>>v1 = VectorV7([1, 2, 3])
>>>v1 * 10
>>>Vector([10.0, 20.0, 30.0])
11 * v1
>>>Vector([11.0, 22.0, 33.0])
>>>``va = VectorV7([1, 2, 3])
>>>vz = VectorV7([5, 6, 7])
>>>va @ vz
38.0
>>>[10, 20, 30] @ vz
380.0
```

### 16.3 算术运算符总结

| 运算符    | 正向方法     | 反向方法      | 就地方法      | 说明                           |
| --------- | ------------ | ------------- | ------------- | ------------------------------ |
| +         | __add__      | __radd__      | __iadd__      | 加法或拼接                     |
| -         | __sub__      | __rsub__      | __isub__      | 减法                           |
| *         | __mul__      | __rmul__      | __imul__      | 乘法或重复复制                 |
| /         | __truediv__  | __rtruediv__  | __itruediv__  | 除法                           |
| //        | __floordiv__ | __rfloordiv__ | __ifloordiv__ | 整除                           |
| %         | __mod__      | __rmod__      | __imod__      | 求模                           |
| divmod()  | __divmod__   | __rdivmod__   | __idivmod__   | 返回由整除的商和模数组成的元组 |
| **、pow() | __pow__      | __rpow__      | __ipow__      | 求幂                           |
| @         | __matmul__   | __rmatmul__   | __imatmul__   | 矩阵乘法                       |
| &         | __and__      | __rand__      | __iand__      | 位与                           |
|           |              | __or__        | __ror__       | __ior__                        |
| ^         | __xor__      | __rxor__      | __ixor__      | 位异或                         |
| <<        | __lshift__   | __rlshift__   | __ilshift__   | 按位左移                       |
| >>        | __rshift__   | __rrshift__   | __irshift__   | 按位右移                       |

### 16.4 众多比较运算符

```python
class VectorV8(VectorV7):
    def __eq__(self, other):
        if isinstance(other, self.__class__):
            return (len(self) == len(other) and
                    all(a == b for a, b in zip(self, other)))
        else:
            return NotImplemented
va = VectorV8([1.0, 2.0, 3.0])
vb = VectorV8(range(1, 4))
>>>va == vb
True
t3 = (1, 2, 3)
>>>va == t3
False
```

## 第17章 迭代器、生成器和经典协程

### 17.1 序列可迭代的原因：iter函数

#### 17.1.1 Sentence类第1版：单词序列

```python
import re
import reprlib

RE_WORD = re.compile(r'\w+')


class SentenceV1:

    def __init__(self, text):
        self.text = text
        # 使用正则表达式分割单词
        self.words = RE_WORD.findall(text)

    def __getitem__(self, index):
        return self.words[index]  

    def __len__(self):  
        return len(self.words)

    def __repr__(self):
        return 'Sentence(%s)' % reprlib.repr(self.text) 
s = SentenceV1('"The time has com," the Walrus said,')
sCopy to clipboardErrorCopied
Sentence('"The time ha... Walrus said,')
for word in s:
    print(word, end=" ")
The time has com the Walrus said 
>>>list(s)
['The', 'time', 'has', 'com', 'the', 'Walrus', 'said']
```

#### 17.1.2 内置函数iter

内置函数`iter`的操作步骤：

1. 检查对象是否实现了`__iter__`方法，如果实现了就调用它，获取一个迭代器。
2. 如果没有实现，但是实现了`__getitem__`方法，那么`iter()`创建一个迭代器，尝试按索引（从0开始）获取项。
3. 如果尝试失败，则Python抛出`TypeError`异常，通常会提示`'C' object is not iterable`（C对象不可迭代），其中C是目标对象所属的类。

`iter()`两种形式：

1. 迭代器：传入两个参数为函数或任何可迭代对象创建迭代器，第一个参数必须是一个可迭代对象，重复调用产生值；第二个参数是哨符（标记值），如果可调用对象返回哨符，则抛出StopIteration，而不产生哨符。
2. 用于构建按块读取工具。

#### 17.1.3 可迭代对象与迭代器

- 可迭代对象的定义： 使用内置的iter可以获取迭代器的对象。如果对象实现了能返回迭代器的`__iter__`方法，那么对象就是可迭代的。序列都可以迭代。实现了`__getitem__`方法，而且接受从0开始的索引，这种对象也是可以迭代的。
- 可迭代对象与迭代器之间的关系：Python从可迭代对象中获取迭代器。

### 17.2 为Sentence类实现`__iter__`方法

#### 17.2.1 Sentence类第2版：经典迭代器

**改进方案：**

1. 删除`__getitem__`方法。
2. 添加`__iter__`方法，初始化`SentenceIterator`类，返回一个迭代器。
3. 添加`SentenceIterator`类，实现`__next__`和`__iter__`方法。

```python
import re
import reprlib

RE_WORD = re.compile(r'\w+')


class SentenceV2:

    def __init__(self, text):
        self.text = text
        self.words = RE_WORD.findall(text)

    def __repr__(self):
        return f'Sentence({reprlib.repr(self.text)})'

    def __iter__(self):
        # 返回一个迭代器
        return SentenceIterator(self.words)


class SentenceIterator:

    def __init__(self, words):
        self.words = words  
        # 初始化索引
        self.index = 0

    def __next__(self):
        try:
            word = self.words[self.index]
        except IndexError:
            raise StopIteration()
        self.index += 1
        return word

    def __iter__(self):  
        return self
```

#### 17.2.2 可迭代对象和迭代器的区别

- 可迭代对象有一个`__iter__`方法，每次都实例化一个新迭代器。
- 迭代器要实现`__next__`方法，返回单个元素，此外还要实现`__iter__`方法，返回迭代器本身。
- 迭代器也是可迭代对象，但是可迭代对象不是迭代器。

#### 17.2.3 Sentence类第3版：生成器函数

**改进方案：**

1. 添加`__iter__`方法：遍历单词数组，使用yield创建生成器。

```python
import re
import reprlib

RE_WORD = re.compile(r'\w+')


class SentenceV3:

    def __init__(self, text):
        self.text = text
        self.words = RE_WORD.findall(text)

    def __repr__(self):
        return 'Sentence(%s)' % reprlib.repr(self.text)

    def __iter__(self):
        for word in self.words:
            # 产生当前的word
            yield word
```

#### 17.2.4 生成器的工作原理

只要Python函数的主体中有`yield`关键字，该函数就是生成器函数。调用生成器函数，返回一个生成器对象。

生成器工作原理：

1. 生成器函数创建一个生成器对象，包装生成器函数的主体。
2. 把生成器对象传给`next()`函数时，生成器函数提前执行函数主体中的下一个`yield`语句，返回产出的值，并在函数主体的当前位置暂停。
3. 函数的主体返回时，Python创建的外层生成器对象抛出`StopIteration`异常。

### 17.3 惰性实现版本

#### 17.3.1 Sentence类第4版：惰性生成器

**改进方案：**

1. 修改`__init__`方法，删除`words`的初始化。
2. 修改`__iter__`方法，用正则表达式分割句子，并用`yield`返回迭代对象。

```python
import re
import reprlib

RE_WORD = re.compile(r'\w+')


class SentenceV4:

    def __init__(self, text):
        self.text = text 

    def __repr__(self):
        return f'Sentence({reprlib.repr(self.text)})'

    def __iter__(self):
        # 产出MatchObject实例
        for match in RE_WORD.finditer(self.text):  
            yield match.group()
```

#### 17.3.2 Sentence类第5版：惰性生成器表达式

**改进方案：**

1. 修改`__iter__`方法：使用生成器表达式构建生成器对象。

```python
import re
import reprlib

RE_WORD = re.compile(r'\w+')


class SentenceV5:

    def __init__(self, text):
        self.text = text

    def __repr__(self):
        return f'Sentence({reprlib.repr(self.text)})'

    def __iter__(self):
        return (match.group() for match in RE_WORD.finditer(self.text))
```

### 17.4 迭代器和生成器

- 迭代器：泛指实现了__next__方法的对象。迭代器用于生成供客户代码使用的数据，即客户代码通过`for`循环或其他迭代方式，或者直接在迭代器上调用``next(it)`驱动迭代器。
- 生成器：由Python编译器构建的迭代器。为了创建生成器，使用`yield`关键字得到生成器函数。生成器表达式是构建生成器对象的另一种方式。

### 17.5 等差数列生成器

#### 17.5.1 自定义的等差数列类`ArithmeticProgression`

```python
class ArithmeticProgression:

    def __init__(self, begin, step, end=None):
        self.begin = begin
        self.step = step
        self.end = end  # None -> "infinite" series

    def __iter__(self):
        result_type = type(self.begin + self.step)
        result = result_type(self.begin)
        forever = self.end is None
        while forever or result < self.end:
            yield result
            result += self.step
>>>ap = ArithmeticProgression(0, 1, 3)
>>>list(ap)
[0, 1, 2]
ap = ArithmeticProgression(1, .5, 3)
>>>list(ap)
[1.0, 1.5, 2.0, 2.5]
```

#### 17.5.2 使用`itertools`模块生成等差数列

```python
import itertools

gen = itertools.takewhile(lambda n: n < 3, itertools.count(1, .5))
list(gen)
[1, 1.5, 2.0, 2.5]
def aritprog_gen(begin, step, end=None):
    first = type(begin + step)(begin)
    ap_gen = itertools.count(first, step)
    if end is None:
        return ap_gen
    return itertools.takewhile(lambda n: n < end, ap_gen)
```

#### 17.5.3 标准库中的生成器函数

```python
# 返回输入的可迭代对象中连续的重叠对
list(itertools.pairwise(range(7)))
[(0, 1), (1, 2), (2, 3), (3, 4), (4, 5), (5, 6)]
# 分组函数
for char, group in itertools.groupby('LLLAAAGG'):
    print(char , '-->', list(group))
L --> ['L', 'L', 'L']
A --> ['A', 'A', 'A']
G --> ['G', 'G']
```

### 17.6 yield from：从子生成器中产出

yield from表达式是把一个生成器的工作委托给一个子生成器。

#### 17.6.1 重新实现chain

```python
def chain(*iterables):
    for it in iterables:
        for i in it:
            yield i
s = 'ABC'
r = range(3)
>>>list(chain(s, r))
['A', 'B', 'C', 0, 1, 2]
# 用yield from重新实现chain
def chain(*iterables):
    for i in iterables:
        yield from i
>>>list(chain(s, r))
['A', 'B', 'C', 0, 1, 2]
```

#### 17.6.2 遍历树状结构

```python
def tree(cls, dis_level, level=0):
    if level <= dis_level:
        yield cls.__name__, level
        for sub_cls in cls.__subclasses__():
            yield from tree(sub_cls, dis_level, level=level+1)


def display(cls, display_level=5):
    for cls_name, level in tree(cls, display_level - 1):
        indent = ' ' * 4 * level
        print(f'{indent}{cls_name}')    
# 显示2层异常层次结构
display(BaseException, 2)
BaseException
    Exception
    GeneratorExit
    SystemExit
    KeyboardInterrupt
    CancelledError
    BaseExceptionGroup
```

### 17.7 经典协程

经典协程的类型提示：`Generator[YieldType, SendType, ReturnType]`

#### 17.7.1 示例：使用协程计算累计平均值

```python
from collections.abc import Generator

def averager() -> Generator[float, float, None]:
    total = 0.0
    count = 0
    average = 0.0
    while True:
        # 暂停执行协程，返回结果
        term = yield average
        total += term
        count += 1
        average = total/count
coro_avg = averager()
>>>next(coro_avg)
0.0
>>>coro_avg.send(10)
10.0
>>>coro_avg.send(30)
20.0
>>>coro_avg.send(5)
15.0
```

#### 17.7.2 返回项数和平均值

```python
from collections.abc import Generator
from typing import Union, NamedTuple

class Result(NamedTuple):
    count: int  # type: ignore  
    average: float

class Sentinel: 
    def __repr__(self):
        return f'<Sentinel>'

STOP = Sentinel()  

SendType = Union[float, Sentinel] 

def averager2(verbose: bool = False) -> Generator[None, SendType, Result]:  
    total = 0.0
    count = 0
    average = 0.0
    while True:
        term = yield
        if verbose:
            print('received:', term)
        # 如果term为哨符，则跳出循环    
        if isinstance(term, Sentinel):
            break
        total += term  
        count += 1
        average = total / count
    # 返回结果    
    return Result(count, average)
def compute():
    # 协程终止的StopIteration异常时获取返回值
    res = yield from averager2(True)
    print('computed:', res)
    return res 
# 创建委托协程的对象
comp = compute()
for v in [None, 10, 20, 30, STOP]: 
    try:
        comp.send(v)  
    except StopIteration as exc:  
        result = exc.value
received: 10
received: 20
received: 30
received: <Sentinel>
computed: Result(count=3, average=20.0)
```

## 第18章 with、match和else块

### 18.1 上下文管理器和with块

#### 18.1.1 with语句

- with语句作用：简化一些常用的try/finally结构，这种结构保证一段代码运行完毕后执行某些操作，finally子句中的代码通常用于释放重要的资源，或者还原临时改变的状态。

```python
import sys

class LookingGlass:

    def __enter__(self):
        self.original_write = sys.stdout.write
        # 打上猴子补丁
        sys.stdout.write = self.reverse_write
        return 'JABBERWOCKY'

    def reverse_write(self, text):
        # 反转参数的内容
        self.original_write(text[::-1])

    def __exit__(self, exc_type, exc_value, traceback):
        # 将原来的方法还原
        sys.stdout.write = self.original_write
        if exc_type is ZeroDivisionError:
            print('Please DO NOT divide by zero!')
            return True
>>>with LookingGlass() as what:
...    print('Alice, Kitty and Snowdrop')
...    print(what)
pordwonS dna yttiK ,ecilA
YKCOWREBBAJ
```

上述打印的结果是反向的。

```python
what
'JABBERWOCKY'
print('Back to normal.')
Back to normal.
```

#### 18.1.2 @contextmanager装饰器

@contextmanager装饰器把简单的生成器函数变成上下文管理器，避免创建类去实现上下文管理器协议。

```python
import contextlib
import sys

@contextlib.contextmanager
def looking_glass():
    # 保留原来的方法
    original_write = sys.stdout.write  

    def reverse_write(text):
        # 反转参数
        original_write(text[::-1])
    
    # 打上猴子补丁
    sys.stdout.write = reverse_write  
    yield 'JABBERWOCKY'
    # 还原方法
    sys.stdout.write = original_write
```

with块终止时，`__exit__`方法执行了：

1. 检查有没有把异常传给`exc_type`，如果有，则调用`gen.throw(exception)`，再生成器函数主体中yield关键字所在的行抛出异常。
2. 否则，调用`next(gen)`，恢复执行生成器函数主体中yield后面的代码。

@contextmanager装饰的生成器也可以做装饰器。

```python
@looking_glass()
def verse():
    print('The time has come')
verse()
emoc sah emit ehT
```

### 18.2 案例分析：lis.py中的模式匹配

需求：完成Scheme的解释器

#### 18.2.1 类型定义

```python
import math
import operator as op
from collections import ChainMap
from itertools import chain
from typing import Any, TypeAlias, NoReturn

# str的别名，表示标识符
Symbol: TypeAlias = str
# 一种简单的句法元素，表示一个数值或一个Symbol
Atom: TypeAlias = float | int | Symbol
# Scheme程序的基本单元，由原子结构和列表（可以嵌套）构成的表达式    
Expression: TypeAlias = Atom | list
```

#### 18.2.2 解释器

```python
def parse(program: str) -> Expression:
    "从字符串中读取Scheme表达式"
    return read_from_tokens(tokenize(program))

def tokenize(s: str) -> list[str]:
    "把字符串转换成词法单元列表"
    return s.replace('(', ' ( ').replace(')', ' ) ').split()

def read_from_tokens(tokens: list[str]) -> Expression:
    "从一系列词法单元中读取表达式"
    if len(tokens) == 0:
        raise SyntaxError('unexpected EOF while reading')
    token = tokens.pop(0)
    if '(' == token:
        exp = []
        while tokens[0] != ')':
            exp.append(read_from_tokens(tokens))
        tokens.pop(0)  # discard ')'
        return exp
    elif ')' == token:
        raise SyntaxError('unexpected )')
    else:
        return parse_atom(token)

def parse_atom(token: str) -> Atom:
    "将数值转成数值类型，将其他符号转成Symbol类型"
    try:
        return int(token)
    except ValueError:
        try:
            return float(token)
        except ValueError:
            return Symbol(token)
>>>parse('(gcd 18 45)')
['gcd', 18, 45]
>>>parse('''
(define double
    (lambda (n)
        (* n 2)))
''')
['define', 'double', ['lambda', ['n'], ['*', 'n', 2]]]
```

#### 18.2.3 环境

1. Environment类，可以把多个字典和其他映射结合起来，使它们在逻辑上显示并表现为一个整体，并支持就地更改项。

```python
class Environment(ChainMap[Symbol, Any]):
    "ChainMap的子类，允许就地更改项"

    def change(self, key: Symbol, value: Any) -> None:
        "找到key在何处定义，更新对应的值"
        for map in self.maps:
            if key in map:
                map[key] = value  # type: ignore[index]
                return
        raise KeyError(key)
inner_env = {'a': 2}
outer_env = {'a': 0, 'b': 1}
env = Environment(inner_env, outer_env)
env['a']
2
env.change('b', 333)
env
Environment({'a': 2}, {'a': 0, 'b': 333})
```

1. standard_env函数，构建Environment，并设置Scheme运算逻辑。

```python
def standard_env() -> Environment:
    "An environment with some Scheme standard procedures."
    env = Environment()
    env.update(vars(math))   # sin, cos, sqrt, pi, ...
    env.update({
            '+': op.add,
            '-': op.sub,
            '*': op.mul,
            '/': op.truediv,
            'quotient': op.floordiv,
            '>': op.gt,
            '<': op.lt,
            '>=': op.ge,
            '<=': op.le,
            '=': op.eq,
            'abs': abs,
            'append': lambda *args: list(chain(*args)),
            'apply': lambda proc, args: proc(*args),
            'begin': lambda *x: x[-1],
            'car': lambda x: x[0],
            'cdr': lambda x: x[1:],
            'cons': lambda x, y: [x] + y,
            'display': lambda x: print(lispstr(x)),
            'eq?': op.is_,
            'equal?': op.eq,
            'filter': lambda *args: list(filter(*args)),
            'length': len,
            'list': lambda *x: list(x),
            'list?': lambda x: isinstance(x, list),
            'map': lambda *args: list(map(*args)),
            'max': max,
            'min': min,
            'not': op.not_,
            'null?': lambda x: x == [],
            'number?': lambda x: isinstance(x, (int, float)),
            'procedure?': callable,
            'round': round,
            'symbol?': lambda x: isinstance(x, Symbol),
    })
    return env
```

#### 18.2.4 REPL

```python
def repl(prompt: str = 'lis.py> ') -> NoReturn:
    "一个提示-读取-求值-输出的循环"
    global_env = Environment({}, standard_env())
    while True:
        # 解析语法树
        ast = parse(input(prompt))
        # 计算结果
        val = evaluate(ast, global_env)
        if val is not None:
            # 展示结果
            print(lispstr(val))

def lispstr(exp: object) -> str:
    "将Python对象转换成Lisp理解的字符串"
    if isinstance(exp, list):
        return '(' + ' '.join(map(lispstr, exp)) + ')'
    else:
        return str(exp)
```

#### 18.2.5 求值函数

```python
KEYWORDS = ['quote', 'if', 'lambda', 'define', 'set!']

def evaluate(exp: Expression, env: Environment) -> Any:
    "在环境中求解表达式"
    match exp:
        case int(x) | float(x):
            # 求解数值
            return x
        case Symbol(var):
            # 求解符号
            return env[var]
        case ['quote', x]:
            # (quoto ...)表达式
            return x
        case ['if', test, consequence, alternative]:
            # if表达式
            if evaluate(test, env):
                return evaluate(consequence, env)
            else:
                return evaluate(alternative, env)
        case ['lambda', [*parms], *body] if body:
            # lambda表达式
            return Procedure(parms, body, env)
        case ['define', Symbol(name), value_exp]:
            # 将value_exp表达式的计算结果定义为name
            env[name] = evaluate(value_exp, env)
        case ['define', [Symbol(name), *parms], *body] if body:
            # 自定义运算表达式
            env[name] = Procedure(parms, body, env)
        case ['set!', Symbol(name), value_exp]:
            # 更改已定义变量的值
            env.change(name, evaluate(value_exp, env))
        case [func_exp, *args] if func_exp not in KEYWORDS:
            # 函数调用
            proc = evaluate(func_exp, env)
            values = [evaluate(arg, env) for arg in args]
            return proc(*values)
        case _:
            raise SyntaxError(lispstr(exp))
evaluate(parse('1.5'), {})
1.5
evaluate(parse('+'), standard_env())
<function _operator.add(a, b, /)>
evaluate(parse('(quote no-such-name)'), standard_env())
'no-such-name'
evaluate(parse('(if (= 3 3) 1 0)'), standard_env())
1
```

#### 18.2.6 实现闭包的Procedure类

```python
class Procedure:
    "用户定义的Scheme过程"

    def __init__(self, parms: list[Symbol], body: list[Expression], env: Environment):
        # 函数名称
        self.parms = parms
        # 主体表达式
        self.body = body
        # 环境
        self.env = env

    def __call__(self, *args: Expression) -> Any:
        # 构建函数名称与参数的映射
        local_env = dict(zip(self.parms, args))
        # 构建新的环境
        env = Environment(local_env, self.env)
        # 迭代表达式，在新环境中求解
        for exp in self.body:
            result = evaluate(exp, env)
        return result
>>>expr = '(lambda (a b) (* (/ a b) 100))'
>>>f = evaluate(parse(expr), standard_env())
>>>f(15, 20)
75.0
```

### 18.3 else语句

- for-else：仅当for循环运行完毕时，才运行else块。
- while-else：仅当while循环因条件为假值而退出时，才运行else块。
- try-else：仅当try块没有抛出异常时，才运行else块。
- EAFP：取得原谅比获得许可容易（Easier to ask for forgiveness than permission）。先假定存在有效的键或属性，如果假设不成立，那么捕获异常。
- LBYL：三思而后行（Look before you leap）。在调用函数或查找属性或键之前，显式测试前提条件。

## 第19章 Python并发模型

### 19.1 核心概念

- 并发：处理多个待定认为，一次处理一个或并行处理多个，直到所有任务最终都成功或失败。并发也叫做多任务处理。
- 并行：同时执行多个计算任务的能力。
- 执行单元：并发执行代码的对象的统称，每个对象的状态和调用栈是独立的，Python原生支持3种执行单元：进程、线程和协程。
- 进程：
  - 计算机程序运行时的一个实例，消耗内存和部分CPU时间。
  - 进程通过管道、套接字或内存映射文件进行通信。
  - 进程可以派生子进程，子进程之间以及与父进程之间是隔离的。
  - 进程支持抢占式多任务处理机制：操作系统调度程序定期抢占（挂起）运行中的进程，让其他进程运行。
- 线程：
  - 单个进程中的执行单元。
  - 通过调用操作系统API，进程可以创建更多线程，执行并发操作。
  - 一个进程内的线程共享相同的内存空间。
- 协程：
  - 可以挂起自身并在以后恢复的函数。
  - 经典协程由生成器函数构建，原生协程使用`async def`定义。
  - 协程支持协作式多任务处理：一个协程必须使用`yield`或`await`关键字显式放弃控制权，另一个协程才可以并发开展工作。
- 队列：一种数据结构，可以放入和取出项，顺序通常是先入先出（FIFO）。独立的执行单元可以通过队列交换引用数据和控制消息。
- 锁：一种供执行单元用来同步操作和避免数据损坏的对象。
- 争用：对有限资源的争夺。当多个执行单元尝试访问共享资源时，就会发生资源争用。

### 19.2 并发的"Hello World"示例

功能：启动一个函数，阻塞3秒，期间在界面上会显示一个旋转的指针动画，当计算结束后，显示结果：`Answer: 42`。

#### 19.2.1 使用线程实现旋转指针

```python
import itertools
import time
from threading import Thread, Event

def spin(msg: str, done: Event) -> None:
    # 循环展示指针字符
    for char in itertools.cycle(r'\|/-'):  
        status = f'\r{char} {msg}'
        print(status, end='', flush=True)
        # 线程阻塞，帧数为10fps
        if done.wait(.1):
            break  
    blanks = ' ' * len(status)
    # 将光标移动到开头，清空状态行
    print(f'\r{blanks}\r', end='')  

def slow() -> int:
    # 停止3秒
    time.sleep(3)
    return 42Copy to clipboardErrorCopied
def supervisor() -> int:
    done = Event()
    spinner = Thread(target=spin, args=('thinking!', done))
    print(f'spinner object: {spinner}')
    # 启动线程
    spinner.start()
    # 调用slow，阻塞main线程
    result = slow()
    # 终止spin函数的for循环
    done.set()
    # 等待，直到spinner线程结束
    spinner.join()
    return result
result = supervisor()
print(f'Answer: {result}')
spinner object: <Thread(Thread-5 (spin), initial)>
Answer: 42  
```

#### 19.2.2 使用进程实现旋转指针

```python
import itertools
import time
from multiprocessing import Process, Event
from multiprocessing import synchronize

def spin(msg: str, done: synchronize.Event) -> None:
    # 循环展示指针字符
    for char in itertools.cycle(r'\|/-'):  
        status = f'\r{char} {msg}'
        print(status, end='', flush=True)
        # 线程阻塞，帧数为10fps
        if done.wait(.1):
            break  
    blanks = ' ' * len(status)
    # 将光标移动到开头，清空状态行
    print(f'\r{blanks}\r', end='')  

def slow() -> int:
    # 停止3秒
    time.sleep(3)
    return 42Copy to clipboardErrorCopied
def supervisor() -> int:
    done = Event()
    spinner = Process(target=spin, args=('thinking!', done))
    print(f'spinner object: {spinner}')
    # 启动线程
    spinner.start()
    # 调用slow，阻塞main线程
    result = slow()
    # 终止spin函数的for循环
    done.set()
    # 等待，直到spinner线程结束
    spinner.join()
    return result
result = supervisor()
print(f'Answer: {result}')
spinner object: <Process name='Process-1' parent=12812 initial>
Answer: 42
```

#### 19.2.3 使用协程实现旋转指针

```python
import itertools
import asyncio

async def spin(msg: str) -> None:
    # 循环展示指针字符
    for char in itertools.cycle(r'\|/-'):  
        status = f'\r{char} {msg}'
        print(status, end='', flush=True)
        try:
            # 线程阻塞，帧数为10fps
            await asyncio.sleep(.1)
        except asyncio.CancelledError:
            break
    blanks = ' ' * len(status)
    # 将光标移动到开头，清空状态行
    print(f'\r{blanks}\r', end='')  

async def slow() -> int:
    # 停止3秒
    await asyncio.sleep(3)
    return 42Copy to clipboardErrorCopied
async def supervisor() -> int:
    # 调度spin最终执行
    spinner = asyncio.create_task(spin('thinking!'))
    print(f'spinner object: {spinner}')  
    # 调用slow，阻塞supervisor，直到slow返回
    result = await slow()
    # 抛出CancelledError异常
    spinner.cancel()
    return result
>>>result = await supervisor()
>>>print(f'Answer: {result}')
spinner object: <Task pending name='Task-6' coro=<spin() running at C:\Users\hurui\AppData\Local\Temp\ipykernel_12812\3509005970.py:4>>
- thinking!Answer: 42
```

- asyncio.run(coro())：在常规函数中调用，驱动一个协程对象，通常作为程序中所有异步代码的入口。
- asyncio.create_task(coro())：在协程中调用，调度另一个协程最终执行。
- await coro()：在协程中调用，把控制权转给coro()返回的协程对象，中止当前协程，直到coro的主体返回。

### 19.3 自建进程池

#### 19.3.1 第1版：素数检测

```python
import math

PRIME_FIXTURE = [
    (2, True),
    (142702110479723, True),
    (299593572317531, True),
    (3333333333333301, True),
    (3333333333333333, False),
    (3333335652092209, False),
    (4444444444444423, True),
    (4444444444444444, False),
    (4444444488888889, False),
    (5555553133149889, False),
    (5555555555555503, True),
    (5555555555555555, False),
    (6666666666666666, False),
    (6666666666666719, True),
    (6666667141414921, False),
    (7777777536340681, False),
    (7777777777777753, True),
    (7777777777777777, False),
    (9999999999999917, True),
    (9999999999999999, False),
]

NUMBERS = [n for n, _ in PRIME_FIXTURE]

def is_prime(n: int) -> bool:
    if n < 2:
        return False
    if n == 2:
        return True
    if n % 2 == 0:
        return False

    root = math.isqrt(n)
    for i in range(3, root + 1, 2):
        if n % i == 0:
            return False
    return TrueCopy to clipboardErrorCopied
from time import perf_counter
from typing import NamedTuple

class Result(NamedTuple):  # <1>
    prime: bool
    elapsed: float

def check(n: int) -> Result:
    # 检查是否为素数
    t0 = perf_counter()
    prime = is_prime(n)
    return Result(prime, perf_counter() - t0)

def main() -> None:
    print(f'Checking {len(NUMBERS)} numbers sequentially:')
    t0 = perf_counter()
    for n in NUMBERS:
        prime, elapsed = check(n)
        label = 'P' if prime else ' '
        print(f'{n:16}  {label} {elapsed:9.6f}s')

    elapsed = perf_counter() - t0  # <4>
    print(f'Total time: {elapsed:.2f}s')
>>>main()
Checking 20 numbers sequentially:
               2  P  0.000001s
 142702110479723  P  0.278544s
 299593572317531  P  0.391379s
3333333333333301  P  1.342821s
3333333333333333     0.000012s
3333335652092209     1.319537s
4444444444444423  P  1.545259s
4444444444444444     0.000002s
4444444488888889     1.485832s
5555553133149889     1.711040s
5555555555555503  P  1.662344s
5555555555555555     0.000006s
6666666666666666     0.000000s
6666666666666719  P  1.868928s
6666667141414921     1.840363s
7777777536340681     2.034407s
7777777777777753  P  1.990972s
7777777777777777     0.000004s
9999999999999917  P  2.309609s
9999999999999999     0.000004s
Total time: 19.79s
```

#### 19.3.2 第2版：基于进程的方案

**改进方案：** 使用多个进程把素数检测分配给多个CPU核。

```python
import sys
from time import perf_counter
from typing import NamedTuple
from multiprocessing import Process, SimpleQueue, cpu_count  
from multiprocessing import queues

class PrimeResult(NamedTuple):
    n: int
    prime: bool
    elapsed: float

# 建立任务队列        
JobQueue = queues.SimpleQueue[int]
ResultQueue = queues.SimpleQueue[PrimeResult]

def check(n: int) -> PrimeResult:
    t0 = perf_counter()
    res = is_prime(n)
    return PrimeResult(n, res, perf_counter() - t0)

def worker(jobs: JobQueue, results: ResultQueue) -> None:
    # 取出要检查的数
    while n := jobs.get():
        # 存放结果
        results.put(check(n))      
    results.put(PrimeResult(0, False, 0.0))

def start_jobs(procs: int, jobs: JobQueue, results: ResultQueue) -> None:
    # 初始化任务队列
    for n in NUMBERS:
        jobs.put(n)
    # 创建多个进程    
    for _ in range(procs):
        proc = Process(target=worker, args=(jobs, results))  
        proc.start()  
        jobs.put(0)

def main(count=-1) -> None:
    if cpu_count != -1:
        procs = count
    else:
        procs = cpu_count()
    
    print(f'Checking {len(NUMBERS)} numbers with {procs} processes:')
    t0 = perf_counter()
    jobs: JobQueue = SimpleQueue()  
    results: ResultQueue = SimpleQueue()
    # 启动任务    
    start_jobs(procs, jobs, results)  
    checked = report(procs, results)
    elapsed = perf_counter() - t0
    print(f'{checked} checks in {elapsed:.2f}s')  

def report(procs: int, results: ResultQueue) -> int: 
    checked = 0
    procs_done = 0
    # 在所有进程都结束之前一直循环
    while procs_done < procs:
        n, prime, elapsed = results.get()
        if n == 0:  # <9>
            procs_done += 1
        else:
            checked += 1
            label = 'P' if prime else ' '
            print(f'{n:16}  {label} {elapsed:9.6f}s')
    return checked
```

### 19.4 Python的多核应用

- 系统管理：Pyhton广泛用于管理大型服务器集群、路由器、负载均衡程序和网络接入存储。使用Python脚本发送命令，由远程设备执行，实现配置任务自动化。
- 数据科学：
  - Jupyter项目：提供两个基于游览器的界面（Jupyter Notebook和JupyterLab），供用户运行和记录可在远程计算机上通过网络运行的分析代码。
  - TensorFlow和PyTorch：深度学习框架。
  - Dask：并行计算库，可以把工作委托给本地进程或设备集群。可以在JupyterLab或Jupyter Notebook中使用，利用Boken不仅可以实现数据可视化，还可以实现交互式仪表板，以接近实时的方式显示数据流和跨进程、跨设备的计算。
- 服务器端Web和移动开发：Python广泛用于Web应用程序开发和为移动应用程序提供支持的后端API开发。
  - 一个应用程序服务器，在Python应用程序的多个实例之间分配负载。
  - 一个任务队列，提供易于使用的高级API，为设备中运行的进程分配任务。
- WSGI应用程序服务器：WSGI是Python框架或应用程序接收HTTP服务器请求并向其发送响应的标准API。

### 19.5 任务队列

任务队列的用途：

- 运行后台作业。
- 在Web请求完成后执行某些操作。
- 异步执行某些操作，失败后重试，确保操作一定完成。
- 安排定期工作。

任务队列的特点：支持横向伸缩。

## 第20章 并发执行器

### 20.1 并发网络下载

#### 20.1.1 依序下载版本

```python
import time
from pathlib import Path
from typing import Callable

import httpx

POP20_CC = ('CN IN US ID BR PK NG BD RU JP '
            'MX PH VN ET EG DE IR TR CD FR').split()

# 存放国旗图像的网络资源
BASE_URL = 'https://www.fluentpython.com/data/flags'
# 保存图像的本地目录
DEST_DIR = Path('downloaded')                         

def save_flag(img: bytes, filename: str) -> None: 
    (DEST_DIR / filename).write_bytes(img)

def get_flag(cc: str) -> bytes:  # <6>
    url = f'{BASE_URL}/{cc}/{cc}.gif'.lower()
    # 建立网络响应
    resp = httpx.get(url, timeout=6.1, follow_redirects=True)  
    resp.raise_for_status()
    return resp.content

def download_many(cc_list: list[str]) -> int:
    # 依序下载
    for cc in sorted(cc_list):                 
        image = get_flag(cc)
        save_flag(image, f'{cc}.gif')
        print(cc, end=' ', flush=True)         
    return len(cc_list)

def main(downloader: Callable[[list[str]], int]) -> None:
    # 创建目录
    DEST_DIR.mkdir(exist_ok=True)                          
    # 记录并报告downloader运行时间
    t0 = time.perf_counter()                               
    count = downloader(POP20_CC)
    elapsed = time.perf_counter() - t0
    print(f'\n{count} downloads in {elapsed:.2f}s')
>>>main(download_many)
BD BR CD CN DE EG ET FR ID IN IR JP MX NG PH PK RU TR US VN 
20 downloads in 14.90s
```

#### 20.1.2 使用concurrent.futures模块下载

```python
from concurrent import futures

def download_one(cc: str):
    # 下载单个图像
    image = get_flag(cc)
    save_flag(image, f'{cc}.gif')
    print(cc, end=' ', flush=True)
    return cc


def download_many(cc_list: list[str]) -> int:
    # 使用ThreadPoolExcutor作为上下文管理器
    with futures.ThreadPoolExecutor() as executor:  
        # 在多个线程中并发调用
        res = executor.map(download_one, sorted(cc_list))  

    return len(list(res))
>>>main(download_many)
ID ET MX BD DE PH US IN JP NG TR VN RU FR PKBR  CN CD IR EG 
20 downloads in 0.99s
```

#### 20.1.3 future对象

- future对象不应自己动手创建，只能由并发框架实例化。future对象表示终将运行的操作，必须排期运行。
- `.done()`方法：该方法不阻塞，返回一个布尔值，指明future对象包装的可调用对象是否已经执行。
- `.result()`方法：当future对象运行结束后，返回可调用对象的结果，或者重新抛出执行可调用对象时抛出的异常。
- `Executor.map`方法：返回一个迭代器，迭代器的`__next__`方法调用各个future对象的`result`方法。

### 20.2 使用concurrent.futures启动进程

```python
from time import sleep, strftime
from concurrent import futures

def display(*args):
    # 打印时间戳
    print(strftime('[%H:%M:%S]'), end=' ')
    print(*args)

def loiter(n):  
    # 在开始时显示一个消息，休眠n秒，在结束时再显示一个消息
    msg = '{}loiter({}): doing nothing for {}s...'
    display(msg.format('\t'*n, n, n))
    sleep(n)
    msg = '{}loiter({}): done.'
    display(msg.format('\t'*n, n))
    return n * 10

def main():
    display('Script starting.')
    # 创建进程池，3个worker
    executor = futures.ThreadPoolExecutor(max_workers=3)  
    # 把5个任务提交给executor
    results = executor.map(loiter, range(5))  
    display('results:', results) 
    display('Waiting for individual results:')
    for i, result in enumerate(results):  
        display(f'result {i}: {result}')
>>>main()
[14:58:48] Script starting.
[14:58:48] loiter(0): doing nothing for 0s...
[14:58:48] loiter(0): done.
[14:58:48]     loiter(1): doing nothing for 1s...
[14:58:48]         loiter(2): doing nothing for 2s...
[14:58:48]             loiter(3): doing nothing for 3s...
[14:58:48] results: <generator object Executor.map.<locals>.result_iterator at 0x000001EC5608ED50>
[14:58:48] Waiting for individual results:
[14:58:48] result 0: 0
[14:58:49]     loiter(1): done.
[14:58:49]                 loiter(4): doing nothing for 4s...
[14:58:49] result 1: 10
[14:58:50]         loiter(2): done.
[14:58:50] result 2: 20
[14:58:51]             loiter(3): done.
[14:58:51] result 3: 30
[14:58:53]                 loiter(4): done.
[14:58:53] result 4: 40
```

## 第21章 异步编程

### 21.1 核心概念

- 原生协程：使用`async def`定义的协程函数。在原生协程内可以使用`await`关键字委托另一个原生协程。`await`关键字不能再原生协程外部使用。
- 经典协程：一种生成器函数，在表达式中使用`yield`读取`my_coro.send(data)`调用发送的数据，可以使用`yield from`委托其他经典协程。
- 基于生成器的协程：使用`@type.coroutine`装饰的生成器函数。
- 异步生成器：使用`async def`定义，而且在主体中使用`yield`的生成器函数，返回一个提供`__anext__`方法的异步生成器对象。

### 21.2 一个asyncio示例：探测域名

```python
import asyncio
import socket
from keyword import kwlist

MAX_KEYWORD_LEN = 4


async def probe(domain: str) -> tuple[str, bool]:
    # 返回一个元组，包含域名和一个布尔值，True表示域名可解析
    loop = asyncio.get_running_loop()
    try:
        # 获取asyncio事件循环的引用
        await loop.getaddrinfo(domain, None)
    except socket.gaierror:
        return (domain, False)
    return (domain, True)

async def main() -> None:
    names = (kw for kw in kwlist if len(kw) <= MAX_KEYWORD_LEN)
    domains = (f'{name}.dev'.lower() for name in names)
    coros = [probe(domain) for domain in domains]
    for coro in asyncio.as_completed(coros):
        domain, found = await coro
        mark = '+' if found else ' '
        print(f'{mark} {domain}')
>>>await main()
+ del.dev
+ try.dev
+ and.dev
+ as.dev
+ in.dev
+ def.dev
+ not.dev
  none.dev
+ from.dev
  true.dev
  else.dev
  if.dev
  is.dev
  with.dev
  pass.dev
  elif.dev
  or.dev
  for.dev
```

### 21.3 使用asyncio和HTTPX下载

```python
import time
from pathlib import Path
from typing import Callable

import httpx

POP20_CC = ('CN IN US ID BR PK NG BD RU JP '
            'MX PH VN ET EG DE IR TR CD FR').split()

# 存放国旗图像的网络资源
BASE_URL = 'https://www.fluentpython.com/data/flags'
# 保存图像的本地目录
DEST_DIR = Path('downloaded')                         

def save_flag(img: bytes, filename: str) -> None: 
    (DEST_DIR / filename).write_bytes(img)

def main(downloader: Callable[[list[str]], int]) -> None:
    # 创建目录
    DEST_DIR.mkdir(exist_ok=True)                          
    # 记录并报告downloader运行时间
    t0 = time.perf_counter()                               
    count = downloader(POP20_CC)
    elapsed = time.perf_counter() - t0
    print(f'\n{count} downloads in {elapsed:.2f}s')
import asyncio

from httpx import AsyncClient

def download_many(cc_list: list[str]) -> int:
    return asyncio.run(supervisor(cc_list))    

async def supervisor(cc_list: list[str]) -> int:
    # AsyncClient提供了异步设置和清理方法的上下文管理器
    async with AsyncClient() as client:          
        to_do = [download_one(client, cc)
                 for cc in sorted(cc_list)]      
        # 等待全部执行完毕，以可异步调用对象的提交顺序返回结果列表
        res = await asyncio.gather(*to_do)       

    return len(res)                              
async def download_one(client: AsyncClient, cc: str):
    image = await get_flag(client, cc)
    save_flag(image, f'{cc}.gif')
    print(cc, end=' ', flush=True)
    return cc

async def get_flag(client: AsyncClient, cc: str) -> bytes:
    url = f'{BASE_URL}/{cc}/{cc}.gif'.lower()
    # httpx.AsyncClient实例的get方法返回一个ClientResponse对象
    resp = await client.get(url, timeout=6.1, follow_redirects=True)  
    return resp.read()
```

### 21.4 增强asyncio版下载脚本的功能

功能：把几个协程传给`asyncio.gather`，按照协程的提交顺序返回协程的结果构成的列表。

代码：`assets/20-executors/getflags/flags2_asyncio.py`

Python中的信号量：

- `asyncio.Semaphore`有一个内部计数器，每次使用`await`处理协程方法`.acquire()`，计数器递减；每次调用`.release()`方法，计数器递增。
- 若计数器大于零，则使用`await`处理`.acquire()`方法没有延迟；若计数器为零，则`.acquire()`中止待处理的协程，直到其他协程在同一个`Semaphore`实例上调用`.release()`，递增计数器。

### 21.5 使用asyncio编写服务器

功能：用户通过unicodedata模块中Unicode字符标准名称所包含的单词，在服务器中查询Unicode字符，游览器显示搜索结果。

项目启动：`nvicorn web_mojifinder:app --reload`

- `web_mojifinder:app`：包名、一个冒号和包内定义的ASGI应用程序的名称。
- `--reload`：让uvicorn监控应用程序源文件的变化，自动重新加载。只在开发过程中有用。

### 21.6 异步迭代和异步可迭代对象

- `async for`处理异步可迭代对象，实现了`__aiter__`对象，然而`__aiter__`必须是常规方法（不是协程方法），而且必须返回一个异步迭代器。
- 异步迭代器提供`__anext__`协程方法，返回一个可异步调用对象，也实现`__aiter__`，返回`self`。

#### 21.6.1 异步生成器函数

1. Python异步控制台，使用命令行选项`-m asyncio`运行解释器，可以得到一个异步REPL。
2. 实现一个异步生成器：使用`async for`实现。

```python
import asyncio
import socket
from collections.abc import Iterable, AsyncIterator
from typing import NamedTuple, Optional


class Result(NamedTuple): 
    domain: str
    found: bool


# 设置别名 
OptionalLoop = Optional[asyncio.AbstractEventLoop]


async def probe(domain: str, loop: OptionalLoop = None) -> Result:
    if loop is None:
        loop = asyncio.get_running_loop()
    try:
        await loop.getaddrinfo(domain, None)
    except socket.gaierror:
        return Result(domain, False)
    return Result(domain, True)

# 异步生成器函数产生一个异步生成器对象
async def multi_probe(domains: Iterable[str]) -> AsyncIterator[Result]:  
    loop = asyncio.get_running_loop()
    # 构建一个probe协程对象列表，对应各个域名
    coros = [probe(domain, loop) for domain in domains]
    for coro in asyncio.as_completed(coros):
        # 等待协程对象，获取结果
        result = await coro 
        yield result  
async def main(tld: str) -> None:
    tld = tld.strip('.')
    # 生成长度不超过4的关键字
    names = (kw for kw in kwlist if len(kw) <= 4)
    # 使用指定的顶级域名生成一组域名
    domains = (f'{name}.{tld}'.lower() for name in names)
    print('FOUND\t\tNOT FOUND')  
    print('=====\t\t=========')
    async for domain, found in multi_probe(domains):  
        indent = '' if found else '\t\t'
        print(f'{indent}{domain}')
>>>await main('org')
FOUND        NOT FOUND
=====        =========
pass.org
def.org
in.org
for.org
not.org
true.org
del.org
none.org
from.org
or.org
and.org
elif.org
try.org
else.org
with.org
        is.org
        as.org
        if.org
```

1. 异步生成器用作上下文管理器。

```python
from contextlib import asynccontextmanager

def download_webpage(url):
    print('Download webpage', url)

def update_stats(url):
    print('Update stats', url)
    
def process(data):
    print('Process', data)
    

@asynccontextmanager
async def web_page(url):
    loop = asyncio.get_running_loop()
    data = await loop.run_in_executor(None, download_webpage, url)
    yield data
    await loop.run_in_executor(None, update_stats, url)
    
async with web_page('google.com') as data:
    process(data)
Download webpage google.com
Process None
Update stats google.com
```

1. 异步生成器和原生协程之间的主要异同点
   - 都使用`async def`声明。
   - 异步生成器的主体中肯定有一个`yield`表达式，原生协程中不会有。
   - 原生协程可能返回`None`之外的值，异步生成器只能使用空`return`语句。
   - 原生协程是可异步调用对象，可由`await`表达式驱动，也可以传给`asyncio`库中众多接受可异步调用对象的函数。异步生成器不是可异步调用对象，而是异步可迭代对象，由`async for`或异步推导式驱动。

#### 21.6.2 异步生成器表达式和异步推导式

- 异步生成器表达式可在程序的任何位置定义，但是只能在原生协程或异步生成器函数内使用。
- 异步推导式只能出现在`async def`主体内，或者是异步控制台中。

### 21.7 asyncio之外的异步世界：Curio

使用Curio重写blogdom.py脚本

```python
from curio import run, TaskGroup
import curio.socket as socket
from keyword import kwlist

MAX_KEYWORD_LEN = 4


async def probe(domain: str) -> tuple[str, bool]: 
    try:
        await socket.getaddrinfo(domain, None)
    except socket.gaierror:
        return (domain, False)
    return (domain, True)

async def main() -> None:
    names = (kw for kw in kwlist if len(kw) <= MAX_KEYWORD_LEN)
    domains = (f'{name}.dev'.lower() for name in names)
    # TaskGroup用于监控和控制多个协程，确保协程全部执行并得到清理
    async with TaskGroup() as group:
        for domain in domains:
            # 启动协程，由TaskGroup实例管理
            await group.spawn(probe, domain)
        # 迭代TaskGroup，完成任务之后产出Task实例    
        async for task in group:
            domain, found = task.result
            mark = '+' if found else ' '
            print(f'{mark} {domain}')
>>>run(main())
+ as.dev
+ and.dev
+ def.dev
+ in.dev
+ del.dev
+ not.dev
+ from.dev
+ try.dev
  true.dev
  elif.dev
  else.dev
  if.dev
  is.dev
  none.dev
  with.dev
  pass.dev
  or.dev
  for.dev
```

Curio的特色：

- Curio中的`TaskGroup`是异步上下文管理器，取代了`asyncio`的多个特有API和编程模式。任务组支持结构化并发。
- 对在同一份基准代码中使用协程和线程编程提供了更好的支持。
- 提供了一个`UniversalQueue`，可用于协调线程、Curio协程和`asyncio`协程之间的工作。

### 21.8 异步原理与陷阱

陷阱：

- 规范的异步编程方法可以提升服务器的性能。
- 没有所谓的“I/O密集型系统”，可能遇到的是I/O密集型函数。

发现CPU占用出现瓶颈后，可以采取以下措施：

- 把任务委托给Python进程池。
- 把任务委托给外部任务队列。
- 使用Cython、C、Rust，或者可编译成机器码、能与Python/C API交互的其他语言重写相关代码。
- 如果判断自己可以承受性能损失，可以什么都不做，把决定记录下来，方便以后重新审视。

## 第22章 动态属性和特性

- 数据属性和方法统称为属性。方法是可调用的属性。
- 动态属性的接口和数据属性一样，按需计算。
- 用户定义的类通过`__getattr__`方法可以实现动态属性。

### 22.1 使用动态属性转换数据

#### 22.1.1 FrozenJson第1版

```python
from collections import abc


class FrozenJSON_V1:
    """一个只读接口，该接口使用属性表示法访问JSON类对象"""

    def __init__(self, mapping):
        # 私有属性，构建字典
        self.__data = dict(mapping)

    def __getattr__(self, name):
        """当未指定名称的属性，调用该方法"""
        try:
            # 如果能匹配到字典的某个值，就返回对应的属性
            return getattr(self.__data, name)  
        except AttributeError:
            # 否则，从字典中获取name对应的项，返回调用build方法得到的结果
            return self.__class__.build(self.__data[name])  # <4>

    def __dir__(self):
        # 支持在Python控制台进行自动补全
        return self.__data.keys()

    @classmethod
    def build(cls, obj):
        if isinstance(obj, abc.Mapping):
            # 如果是一个map，则构建一个FrozenJSON对象，大鹅类型
            return cls(obj)
        elif isinstance(obj, abc.MutableSequence):
            # 如果是列表，将obj的每一项进行递归构建列表
            return [cls.build(item) for item in obj]
        else:
            return obj
>>>import json
>>>raw_feed = json.load(open('./data/osconfeed.json'))
>>>feed = FrozenJSON_V1(raw_feed)
>>>len(feed.Schedule.speakers)
357
>>>feed.keys()
>>>dict_keys(['Schedule'])
>>>sorted(feed.Schedule.keys())
['conferences', 'events', 'speakers', 'venues']
>>>for key, value in sorted(feed.Schedule.items()):
...    print(f'{len(value):3} {key}')
  1 conferences
484 events
357 speakers
 53 venues
```

#### 22.1.2 FrozenJSON第2版

修改`__init__`方法，解决与Python关键字同名的属性名问题。

```python
from collections import abc
import keyword

class FrozenJSON_V2:
    """一个只读接口，该接口使用属性表示法访问JSON类对象"""

    def __init__(self, mapping):
        self.__data = {}
        for key, value in mapping.items():
            if keyword.iskeyword(key):
                key += '_'
            self.__data[key] = value

    def __getattr__(self, name):
        """当未指定名称的属性，调用该方法"""
        try:
            # 如果能匹配到字典的某个值，就返回对应的属性
            return getattr(self.__data, name)  
        except AttributeError:
            # 否则，从字典中获取name对应的项，返回调用build方法得到的结果
            return self.__class__.build(self.__data[name])  # <4>

    def __dir__(self):
        # 支持在Python控制台进行自动补全
        return self.__data.keys()

    @classmethod
    def build(cls, obj):
        if isinstance(obj, abc.Mapping):
            # 如果是一个map，则构建一个FrozenJSON对象，大鹅类型
            return cls(obj)
        elif isinstance(obj, abc.MutableSequence):
            # 如果是列表，将obj的每一项进行递归构建列表
            return [cls.build(item) for item in obj]
        else:
            return objCopy to clipboardErrorCopied
student = FrozenJSON_V2({'name': 'Jim Bo', 'class': 1982})
```

#### 22.1.3 FrozenJSON

使用`__new__`代替`build`方法。

```python
from collections import abc
import keyword

class FrozenJSON_V3:
    """一个只读接口，该接口使用属性表示法访问JSON类对象"""
    def __new__(cls, arg):
        if isinstance(arg, abc.Mapping):
            # 如果是一个map，则构建一个FrozenJSON对象，大鹅类型
            return super().__new__(cls)
        elif isinstance(arg, abc.MutableSequence):
            # 如果是列表，将obj的每一项进行递归构建列表
            return [arg(item) for item in arg]
        else:
            return arg 
    
    
    def __init__(self, mapping):
        self.__data = {}
        for key, value in mapping.items():
            if keyword.iskeyword(key):
                key += '_'
            self.__data[key] = value

    def __getattr__(self, name):
        """当未指定名称的属性，调用该方法"""
        try:
            # 如果能匹配到字典的某个值，就返回对应的属性
            return getattr(self.__data, name)  
        except AttributeError:
            # 否则，从字典中获取name对应的项，返回调用build方法得到的结果
            return self.__class__(self.__data[name])  # <4>

    def __dir__(self):
        # 支持在Python控制台进行自动补全
        return self.__data.keys()
```

### 22.2 计算特性

#### 22.2.1 第1步：数据驱动属性创建

目标：通过speakers的编号获取对应的数据。

```python
import json

JSON_PATH = './data/osconfeed.json'

class Record:
    def __init__(self, **kwargs):
        # 根据关键字参数构建带属性的实例
        self.__dict__.update(kwargs)  

    def __repr__(self):
        return f'<{self.__class__.__name__} serial={self.serial!r}>'  # <2>

def load(path=JSON_PATH):
    records = {}  
    # 解析JSON字符串
    with open(path) as fp:
        raw_data = json.load(fp)  
    # 迭代4个顶级列表    
    for collection, raw_records in raw_data['Schedule'].items():
        record_type = collection[:-1]  
        for raw_record in raw_records:
            key = f'{record_type}.{raw_record["serial"]}' 
            records[key] = Record(**raw_record)  
    return records
>>>records = load(JSON_PATH)
>>>speaker = records['speaker.3471']
>>>speaker
<Record serial=3471>
>>>speaker.name, speaker.twitter
('Anna Martelli Ravenscroft', 'annaraven')
```

#### 22.2.2 第2步：通过特性获取链接的记录

目标：给定一个`event`记录，读取`venue`特性得到一个`Record`对象。

```python
import inspect  # <1>
import json

JSON_PATH = './data/osconfeed.json'

class Record:
    # 存放对load函数返回的字典的引用
    __index = None

    def __init__(self, **kwargs):
        self.__dict__.update(kwargs)

    def __repr__(self):
        return f'<{self.__class__.__name__} serial={self.serial!r}>'

    @staticmethod 
    def fetch(key):
        if Record.__index is None:
            # 如果没有键，则从解析加载
            Record.__index = load()
        return Record.__index[key]
class Event(Record):

    def __repr__(self):
        try:
            # 如果实例有name属性，则设置字符串表示形式
            return f'<{self.__class__.__name__} {self.name!r}>'  # <2>
        except AttributeError:
            return super().__repr__()

    @property
    def venue(self):
        # 根据venue_serial属性构建一个Key，传给fetch方法
        key = f'venue.{self.venue_serial}'
        return self.__class__.fetch(key)
def load(path=JSON_PATH):
    records = {}
    with open(path) as fp:
        raw_data = json.load(fp)
    for collection, raw_records in raw_data['Schedule'].items():
        # 删除尾部s
        record_type = collection[:-1]
        # 首字母大写，用于适配类名
        cls_name = record_type.capitalize()  
        cls = globals().get(cls_name, Record)  
        if inspect.isclass(cls) and issubclass(cls, Record):
            factory = cls
        else:
            factory = Record
        for raw_record in raw_records:
            key = f'{record_type}.{raw_record["serial"]}'
            records[key] = factory(**raw_record)
    return records
>>>event = Record.fetch('event.33950')
>>>event
<Event 'There *Will* Be Bugs'>
>>>event.venue
<Record serial=1449>
>>>event.venue.name
'Portland 251'
>>>event.venue_serial
1449
```

#### 22.2.3 第3步：用特性覆盖现有属性

```python
class Event(Record):

    def __repr__(self):
        try:
            return f'<{self.__class__.__name__} {self.name!r}>'
        except AttributeError:
            return super().__repr__()

    @property
    def venue(self):
        key = f'venue.{self.venue_serial}'
        return self.__class__.fetch(key)

    @property
    def speakers(self):
        spkr_serials = self.__dict__['speakers']
        fetch = self.__class__.fetch
        # 获取键与spkr_serials中的数值匹配的所有记录，构成一个列表
        return [fetch(f'speaker.{key}')
                for key in spkr_serials]
```

- 直接通过对象的`__dict__`属性读写数据，是Python元编程常见的技巧。

#### 22.2.4 第4步：自己实现特性缓存

```python
class Event(Record):

    def __init__(self, **kwargs):
        # 禁用键共享优化
        self.__speaker_objs = None
        super().__init__(**kwargs)

    def __repr__(self):
        try:
            return f'<{self.__class__.__name__} {self.name!r}>'
        except AttributeError:
            return super().__repr__()

    @property
    def venue(self):
        key = f'venue.{self.venue_serial}'
        return self.__class__.fetch(key)

    @property
    def speakers(self):
        # 实现缓存
        if self.__speaker_objs is None:
            spkr_serials = self.__dict__['speakers']
            fetch = self.__class__.fetch
            self.__speaker_objs = [fetch(f'speaker.{key}')
                    for key in spkr_serials]
        return self.__speaker_objs
```

#### 22.2.5 第5步：使用functools缓存特性

- `functools.cached_property`装饰器把方法的结果缓存在同名实例属性中。
- `@cached_property`装饰器不创建完整的特性，而是创建一个非覆盖型描述符。
- `cached_property()`允许属性写入。
- `@cached_property`装饰器仅在执行查找且不村子啊同名属性时允许，一旦允许，就会写入同名属性。
- 缓存的值可以通过删除属性清空。

```python
from functools import cached_property, cache

class Event(Record):

    def __repr__(self):
        try:
            return f'<{self.__class__.__name__} {self.name!r}>'
        except AttributeError:
            return super().__repr__()

    @cached_property
    def venue(self):
        key = f'venue.{self.venue_serial}'
        return self.__class__.fetch(key)
    
    @property  
    @cache
    def speakers(self):
        spkr_serials = self.__dict__['speakers']
        fetch = self.__class__.fetch
        return [fetch(f'speaker.{key}')
                for key in spkr_serials]
```

### 22.3 使用特性验证属性

需求：假设有一个销售散装有机食物的电商应用程序，客户可以按量订购坚果、干果或杂粮。在这个系统中，每个订单中有一系列的商品。

#### 22.3.1 LineItem类第1版：表示订单中商品的类

```python
class LineItem:

    def __init__(self, description, weight, price):
        self.description = description
        self.weight = weight
        self.price = price

    def subtotal(self):
        return self.weight * self.price
>>>raisins = LineItem('Golden raisins', 10, 6.95)
>>>raisins.subtotal()
69.5
>>>raisins.weight = -20
>>>raisins.subtotal()
-139.0
```

#### 22.3.2 LineItem类第2版：能验证值的特性

问题：数据可能会被设置为负值，引发无效输出。

```python
class LineItem:

    def __init__(self, description, weight, price):
        self.description = description
        self.weight = weight 
        self.price = price

    def subtotal(self):
        return self.weight * self.price

    @property  
    def weight(self):  
        return self.__weight  

    @weight.setter 
    def weight(self, value):
        if value > 0:
            self.__weight = value  
        else:
            raise ValueError('value must be > 0')  
```

### 22.4 定义一个特性工厂函数

目标：保护LineItem对象的weight属性和price属性，只允许设为大于0的值，但是不用手动实现两对几乎一样的读值和设值方法。

```python
def quantity(storage_name):
    """特性工厂函数
    storage_name: 确定各个特性的数据存储在哪里
    """
    def qty_getter(instance):
        return instance.__dict__[storage_name]

    def qty_setter(instance, value):
        if value > 0:
            instance.__dict__[storage_name] = value
        else:
            raise ValueError('value must be > 0')
    # 构建一个自定义的特性对象
    return property(qty_getter, qty_setter)
class LineItem:
    # 定义为类属性
    weight = quantity('weight')  
    price = quantity('price') 

    def __init__(self, description, weight, price):
        self.description = description
        self.weight = weight  
        self.price = price

    def subtotal(self):
        return self.weight * self.price  
>>>nutmeg = LineItem('Moluccan nutmeg', 8, 13.95)
>>>nutmeg.weight, nutmeg.price
(8, 13.95)
>>>nutmeg.__dict__
{'description': 'Moluccan nutmeg', 'weight': 8, 'price': 13.95}
```

### 22.5 处理属性的重要属性和函数

#### 22.5.1 影响属性处理方式的特殊属性

- `__class__`：对象所属类的引用。Python的某些特殊方法，只在对象的类中而不在实例中寻找。
- `__dict__`：存储对象或类的可写属性的映射。在任何时候都能随意设置新属性。
- `__slots__`：类可以定义这个属性，节省内存。

#### 22.5.2 处理属性的内置函数

- `dir([object])`：列出对象的大多数属性。`dir`函数不列出`__dict__`属性本书，但会列出其中的键。
- `getattr(object, name[, default])`：从`object`对象中获取`name`字符串对应的属性。主要用于获取事先不知道名称的属性。属性可能来自对象所属的类或超类。
- `hasattr(object, name)`：如果`object`对象中存在指定的属性，或者能以某种方式（例如继承）通过`object`对象获取指定的属性，则返回`True`。
- `setattr(object, name, value)`：把`object`对象指定属性的值设为`value`。
- `vars([object])`：返回`object`对象的`__dict__`属性。

#### 22.5.3 处理属性的特殊方法

- `__delattr__(self, name)`：只要使用`del`语句删除属性，就会调用这个方法。
- `__dir__(self)`：在对象上调用`dir`函数时，会调用这个方法。
- `__getattr__(self, name)`：仅当获取指定的属性失败，搜索过`obj`、`Class`及其超类之后，会调用这个方法。
- `__getattribute__(self, name)`：尝试直接获取指定名称的属性时，始终调用这个方法。
- `__setattr__(self, name, value)`：尝试设置指定名称的属性时，会调用这个方法。

## 第23章 属性描述符

### 23.1 描述符示例：属性验证

#### 23.1.1 描述符相关术语

- 描述符类：实现描述符协议的类。
- 托管类：把描述符实例声明为类属性的类。
- 描述符实例：描述符类的各个实例，声明为托管类的类属性。
- 托管实例：托管类的实例。
- 储存属性：托管实例中存储托管属性的属性。
- 托管属性：托管类中由描述符实例处理的公开属性，值存储在储存属性中。

#### 23.1.2 LineItem类第3版：一个简单的描述符

```python
class Quantity:  # <1>

    def __init__(self, storage_name):
        # 托管实例中用于存储值的储存属性的名称
        self.storage_name = storage_name

    def __set__(self, instance, value):
        # 为托管属性赋值
        if value > 0:
            instance.__dict__[self.storage_name] = value
        else:
            msg = f'{self.storage_name} must be > 0'
            raise ValueError(msg)

    def __get__(self, instance, owner):
        return instance.__dict__[self.storage_name]
class LineItem:
    # 描述符实例管理weight属性
    weight = Quantity('weight')
    # 描述符实例管理price属性
    price = Quantity('price')

    def __init__(self, description, weight, price):
        self.description = description
        self.weight = weight
        self.price = price

    def subtotal(self):
        return self.weight * self.price
try:
    truffle = LineItem('White truffle', 100, 0)
except ValueError as e:
    print(e)
price must be > 0
```

#### 23.1.3 LineItem类第4版：为储存属性自动命名

目标：避免在描述符实例中重复输入属性名。

```python
class Quantity:
    # owner是托管类，name是在owner的类主体中描述符实例赋给的那个属性名
    def __set_name__(self, owner, name):
        self.storage_name = name          

    def __set__(self, instance, value): 
        if value > 0:
            instance.__dict__[self.storage_name] = value
        else:
            msg = f'{self.storage_name} must be > 0'
            raise ValueError(msg)
class LineItem:
    weight = Quantity()
    price = Quantity()

    def __init__(self, description, weight, price):
        self.description = description
        self.weight = weight
        self.price = price

    def subtotal(self):
        return self.weight * self.price
```

#### 23.1.4 LineItem类第5版：一种新型描述符

需求：虚构的有机食物网店遇到了一个问题，有个商品的描述信息为空，导致无法下单。

```python
import abc

class Validated(abc.ABC):

    def __set_name__(self, owner, name):
        self.storage_name = name

    def __set__(self, instance, value):
        value = self.validate(self.storage_name, value)  
        instance.__dict__[self.storage_name] = value

    @abc.abstractmethod
    def validate(self, name, value):
        """return validated value or raise ValueError"""
class Quantity(Validated):
    """数值大于0"""

    def validate(self, name, value):  # <1>
        if value <= 0:
            raise ValueError(f'{name} must be > 0')
        return value
class NonBlank(Validated):
    """字符串至少要包含一个非空字符"""

    def validate(self, name, value):
        value = value.strip()
        if not value: 
            raise ValueError(f'{name} cannot be blank')
        return value  
class LineItem:
    # 描述不能为空
    description = NonBlank()
    weight = Quantity()
    price = Quantity()

    def __init__(self, description, weight, price):
        self.description = description
        self.weight = weight
        self.price = price

    def subtotal(self):
        return self.weight * self.price
```

### 23.2 覆盖型描述符与非覆盖型描述符对比

- 覆盖型描述符：实现`__set__`方法的描述符都属于覆盖型描述符。
- 没有`__get__`方法的覆盖型描述符：当读取时，只要有同名的实例属性，描述符就会被覆盖。
- 非覆盖型描述符：没有实现`__set__`方法的描述符都属于非覆盖型描述符。

### 23.3 方法是描述符

```python
import collections


class Text(collections.UserString):

    def __repr__(self):
        return 'Text({!r})'.format(self.data)

    def reverse(self):
        return self[::-1]
>>>word = Text('forward')
>>>word
Text('forward')
# 反向拼写单词
>>>word.reverse()
Text('drawrof')
# 在类上调用方法相当于调用函数
>>>Text.reverse(Text('backward'))
Text('drawkcab')
# 函数都是非覆盖型描述符
>>>Text.reverse.__get__(word)
<bound method Text.reverse of Text('forward')>
```

### 23.4 描述符用法建议

- 使用property保持简单：内置property类创建的是实现了`__set__`和`__get__`方法的覆盖型描述符。
- 只读描述符必须有`__set__`方法。
- 用于验证的描述符可以只有`__set__`方法。
- 仅有`__get__`方法的描述符可以实现高效缓存：`@functools.cached_property`装饰器创建的就是非覆盖型描述符。
- 非特殊的方法可以被实例属性覆盖：函数和方法只实现了`__get__`方法，属于非覆盖型描述符。

## 第24章 类元编程

### 24.1 类的标准属性

- `cls.__bases__`：由类的基类构成的元组。
- `cls.__qualname__`：类或函数的限定名称，即从模块的全局作用域到类的点分路径。
- `cls.__subclasses__()`：这个方法返回包含类的直接子类的列表，防止在超类和子类之间出现循环引用。返回的列表中是内存里现存的子类，不含尚未导入的模块中的子类。
- `cls.mro()`：构建类时，如果需要获取储存在类属性`__mro__`中的超类元组，会调用这个方法。

### 24.2 type：内置的类工厂函数

```python
class MySuperClass:
    ...
    
class MyMixin:
    ...


MyClass = type('MyClass',
              (MySuperClass, MyMixin),
              {'x': 42, 'x2': lambda self: self.x * 2})
```

type传入的参数：

- name：class关键字后的标识符。
- bases：类标识符后面圆括号内提供的超类元组，如果class语句没有提供超类，则为`(object, )`。
- dict：属性名称到值的映射。

### 24.3 类工厂函数

需求：构建一个简单的工厂函数，用于创建可变对象的类。在一个宠物店应用程序中，以简单的记录存储狗的数据。

```python
from typing import Union, Any
from collections.abc import Iterable, Iterator

# 别名
FieldNames = Union[str, Iterable[str]]

def record_factory(cls_name: str, field_names: FieldNames) -> type[tuple]:
    
    # 使用属性名构建一个元组
    slots = parse_identifiers(field_names)

    def __init__(self, *args, **kwargs) -> None:
        # 接受位置参数和关键字参数
        attrs = dict(zip(self.__slots__, args))
        attrs.update(kwargs)
        for name, value in attrs.items():
            setattr(self, name, value)

    def __iter__(self) -> Iterator[Any]:
        # 按照__slots__设定的顺序产出字段值
        for name in self.__slots__:
            yield getattr(self, name)

    def __repr__(self): 
        values = ', '.join(f'{name}={value!r}'
            for name, value in zip(self.__slots__, self))
        cls_name = self.__class__.__name__
        return f'{cls_name}({values})'
    
    # 组建类属性字典
    cls_attrs = dict(
        __slots__=slots,
        __init__=__init__,
        __iter__=__iter__,
        __repr__=__repr__,
    )
    
    # 调用type构造函数，构建新类
    return type(cls_name, (object,), cls_attrs)
def parse_identifiers(names: FieldNames) -> tuple[str, ...]:
    if isinstance(names, str):
        # 把以空格或逗号分隔的names转成字符串列表
        names = names.replace(',', ' ').split()
    if not all(s.isidentifier() for s in names):
        raise ValueError('names must all be valid identifiers')
    return tuple(names)
>>>Dog = record_factory('Dog', 'name weight owner')
>>>rex = Dog('Rex', 30, 'Bob')
>>>rex
>>>Dog(name='Rex', weight=30, owner='Bob')
"{2}'s dog weighs {1}kg".format(*rex)
"Bob's dog weighs 30kg"
```

### 24.4 Checked类第1版：构建`__init_subclass__`方法

```python
from collections.abc import Callable
from typing import Any, NoReturn, get_type_hints


class Field:
    def __init__(self, name: str, constructor: Callable) -> None:
        # 提示构造函数异常
        if not callable(constructor) or constructor is type(None):
            raise TypeError(f'{name!r} type hint must be callable')
        self.name = name
        self.constructor = constructor

    def __set__(self, instance: Any, value: Any) -> None:
        if value is ...:  
            # 调用无参构造函数
            value = self.constructor()
        else:
            try:
                value = self.constructor(value)  
            except (TypeError, ValueError) as e:  
                type_name = self.constructor.__name__
                msg = f'{value!r} is not compatible with {self.name}:{type_name}'
                raise TypeError(msg) from e
        # 存入__dict__中       
        instance.__dict__[self.name] = value
class Checked:
    @classmethod
    def _fields(cls) -> dict[str, type]: 
        return get_type_hints(cls)

    def __init_subclass__(subclass) -> None:
        # 定义当前类的子类时调用
        super().__init_subclass__()          
        # 构造子类的属性
        for name, constructor in subclass._fields().items():   
            setattr(subclass, name, Field(name, constructor))  

    def __init__(self, **kwargs: Any) -> None:
        # 遍历类的各个name
        for name in self._fields():             
            value = kwargs.pop(name, ...)       
            setattr(self, name, value)          
        if kwargs:
            # 与声明不匹配的名称，提示错误
            self.__flag_unknown_attrs(*kwargs)  

    def __setattr__(self, name: str, value: Any) -> None:
        # 截获一切设置实例属性的操作
        if name in self._fields():              
            cls = self.__class__
            # 如果属性名称是已知的，获取对应的描述符
            descriptor = getattr(cls, name)
            descriptor.__set__(self, value)     
        else:                                   
            self.__flag_unknown_attrs(name)

    def __flag_unknown_attrs(self, *names: str) -> NoReturn:  
        plural = 's' if len(names) > 1 else ''
        extra = ', '.join(f'{name!r}' for name in names)
        cls_name = repr(self.__class__.__name__)
        raise AttributeError(f'{cls_name} object has no attribute{plural} {extra}')

    def _asdict(self) -> dict[str, Any]:
        # 根据子类对象的属性创建字典
        return {
            name: getattr(self, name)
            for name, attr in self.__class__.__dict__.items()
            if isinstance(attr, Field)
        }

    def __repr__(self) -> str:
        kwargs = ', '.join(
            f'{key}={value!r}' for key, value in self._asdict().items()
        )
        return f'{self.__class__.__name__}({kwargs})'
class Movie(Checked):  
    title: str  
    year: int
    box_office: floatCopy to clipboardErrorCopied
movie = Movie(title='The Godfather', year=1972, box_office=137)
movie
Movie(title='The Godfather', year=1972, box_office=137.0)
```

### 24.5 Checked类第2版：使用类装饰器增强类的功能

改进方案：

- 目标：将Checked类改成类装饰器方式。
- 内容：将Checked类中的方法都从类中移出，将Checked用type组装成类装饰器checked。

```python
def _fields(cls: type) -> dict[str, type]:
    return get_type_hints(cls)

def __init__(self: Any, **kwargs: Any) -> None:
    for name in self._fields():
        value = kwargs.pop(name, ...)
        setattr(self, name, value)
    if kwargs:
        self.__flag_unknown_attrs(*kwargs)

def __setattr__(self: Any, name: str, value: Any) -> None:
    if name in self._fields():
        cls = self.__class__
        descriptor = getattr(cls, name)
        descriptor.__set__(self, value)
    else:
        self.__flag_unknown_attrs(name)

def __flag_unknown_attrs(self: Any, *names: str) -> NoReturn:
    plural = 's' if len(names) > 1 else ''
    extra = ', '.join(f'{name!r}' for name in names)
    cls_name = repr(self.__class__.__name__)
    raise AttributeError(f'{cls_name} has no attribute{plural} {extra}')

def _asdict(self: Any) -> dict[str, Any]:
    return {
        name: getattr(self, name)
        for name, attr in self.__class__.__dict__.items()
        if isinstance(attr, Field)
    }

def __repr__(self: Any) -> str:
    kwargs = ', '.join(f'{key}={value!r}' for key, value in self._asdict().items())
    return f'{self.__class__.__name__}({kwargs})'
def checked(cls: type) -> type:
    # 遍历所有属性，构造子类的属性
    for name, constructor in _fields(cls).items():    
        setattr(cls, name, Field(name, constructor))  

    cls._fields = classmethod(_fields)  # type: ignore  
    
    # 被装饰的类的实例方法的模块级函数
    instance_methods = (
        __init__,
        __repr__,
        __setattr__,
        _asdict,
        __flag_unknown_attrs,
    )
    # 将各个函数添加到cls中
    for method in instance_methods:  
        setattr(cls, method.__name__, method)

    return cls 
@checked
class Movie:
    title: str  
    year: int
    box_office: float
movie = Movie(title='The Godfather', year=1972, box_office=137)
movie
Movie(title='The Godfather', year=1972, box_office=137.0)
```

### 24.6 导入时和运行时比较

在导入时，解释器的执行操作：

1. 从上到下一次性解析完`.py`模块的源码，此时可能抛出SyntaxError。
2. 编译生成用于执行的字节码。
3. 执行编译后的模块中的顶层代码。

### 24.7 元类

#### 24.7.1 元类概念

元类是制造类的工厂。type是大多数内置的类和用户定义的类的元类。

```python
class SuperKlass:
    ...
    
class MetaKlass(type):
    ...
    
class Klass(SuperKlass, metaclass=MetaKlass):
    x = 42
    def __init__(self, y):
        self.y = y
```

类初始化的执行步骤：

1. 实现`MetaKlass.__new__`，可以对参数进行审查和修改，然后传给`super().__new__`。最终调用`type.__new__`创建新的类对象。
2. `super().__new__`返回之后，进一步处理新创建的类。
3. 调用`SuperKlass.__init_subclass__`，传入新创建的类，如果有类装饰器，会应用类装饰器。
4. Python把类对象绑定给所在命名空间中的名称（class语句是顶层语句时，所在命名空间通常是模块全局命名空间）。

#### 24.7.2 Bunch元类示例

```python
class MetaBunch(type): 
    # 被当作类方法使用
    def __new__(meta_cls, cls_name, bases, cls_dict):
        # 存放属性名称到默认值的映射
        defaults = {}

        def __init__(self, **kwargs):
            # 把响应的示例属性设为从kwargs中取出的值或默认值
            for name, default in defaults.items():
                setattr(self, name, kwargs.pop(name, default))
            if kwargs:
                extra = ', '.join(kwargs)
                raise AttributeError(f'No slots left for: {extra!r}')

        def __repr__(self):
            rep = ', '.join(f'{name}={value!r}'
                            for name, default in defaults.items()
                            if (value := getattr(self, name)) != default)
            return f'{cls_name}({rep})'
        
        # 初始化新类的命名空间
        new_dict = dict(__slots__=[], __init__=__init__, __repr__=__repr__)
        
        # 迭代用户定义的类的命名空间
        for name, value in cls_dict.items():
            # 如果带双下划线的名称，把对应的项复制到新类的命名空间中
            if name.startswith('__') and name.endswith('__'):  
                if name in new_dict:
                    raise AttributeError(f"Can't set {name!r} in {cls_name!r}")
                new_dict[name] = value
            else:
                # 如果不是，则追加到__slots__中
                new_dict['__slots__'].append(name)
                defaults[name] = value
        # 构建并返回新类        
        return super().__new__(meta_cls, cls_name, bases, new_dict)  


class Bunch(metaclass=MetaBunch):  # <13>
    pass
class Point(Bunch):
    x = 0.0
    y = 0.0
    color = 'gray'
>>>Point(x=1.2, y=3, color='green')
>>>Point(x=1.2, y=3, color='green')
>>>p = Point()
>>>p.x, p.y, p.color
(0.0, 0.0, 'gray')
```

### 24.8 Checked类第3版：使用元类实现

改进方案：

1. 添加一个空的`__slots__`属性，并告诉`CheckMeta.__new__`，这个类不需要特殊处理。
2. 删除`__init_subclass__`，相关工作现在交给`CheckMeta.__new__`。
3. 删除`__setattr__`。

```python
from collections.abc import Callable
from typing import Any, NoReturn, get_type_hints

class Field:
    def __init__(self, name: str, constructor: Callable) -> None:
        if not callable(constructor) or constructor is type(None):
            raise TypeError(f'{name!r} type hint must be callable')
        self.name = name
        # 根据name参数得到带单下划线的storage_name
        self.storage_name = '_' + name 
        self.constructor = constructor

    def __get__(self, instance, owner=None):
        if instance is None:
            return self
        # 返回存储在名为storage_name的属性中的值
        return getattr(instance, self.storage_name)

    def __set__(self, instance: Any, value: Any) -> None:
        if value is ...:
            value = self.constructor()
        else:
            try:
                value = self.constructor(value)
            except (TypeError, ValueError) as e:
                type_name = self.constructor.__name__
                msg = f'{value!r} is not compatible with {self.name}:{type_name}'
                raise TypeError(msg) from e
        # 使用setattr设置或更新托管属性        
        setattr(instance, self.storage_name, value)  
class CheckedMeta(type):

    def __new__(meta_cls, cls_name, bases, cls_dict):
        if '__slots__' not in cls_dict:
            # 仅当类的cls_dict不含__slots__，增强类的功能
            slots = []
            # 得到所有带注解的属性
            type_hints = cls_dict.get('__annotations__', {})
            
            for name, constructor in type_hints.items():
                # 为每个带注解的属性构建一个Field示例
                field = Field(name, constructor)
                # 覆盖cls_dict中相应的项
                cls_dict[name] = field 
                # 把字段的storage_name追加到一个列表中
                slots.append(field.storage_name)  
            # 填充cls_dict中的__slots__项
            cls_dict['__slots__'] = slots
    
        return super().__new__(
                meta_cls, cls_name, bases, cls_dict)  # <9>Copy to clipboardErrorCopied
class Checked(metaclass=CheckedMeta):
    __slots__ = ()  # 跳过CheckedMeta.__new__的处理

    @classmethod
    def _fields(cls) -> dict[str, type]:
        return get_type_hints(cls)

    def __init__(self, **kwargs: Any) -> None:
        for name in self._fields():
            value = kwargs.pop(name, ...)
            setattr(self, name, value)
        if kwargs:
            self.__flag_unknown_attrs(*kwargs)

    def __flag_unknown_attrs(self, *names: str) -> NoReturn:
        plural = 's' if len(names) > 1 else ''
        extra = ', '.join(f'{name!r}' for name in names)
        cls_name = repr(self.__class__.__name__)
        raise AttributeError(f'{cls_name} object has no attribute{plural} {extra}')

    def _asdict(self) -> dict[str, Any]:
        return {
            name: getattr(self, name)
            for name, attr in self.__class__.__dict__.items()
            if isinstance(attr, Field)
        }

    def __repr__(self) -> str:
        kwargs = ', '.join(
            f'{key}={value!r}' for key, value in self._asdict().items()
        )
        return f'{self.__class__.__name__}({kwargs})'
class Movie(Checked):  
    title: str  
    year: int
    box_office: float      
movie = Movie(title='The Godfather', year=1972, box_office=137)
movie
Movie(title='The Godfather', year=1972, box_office=137.0)
```

### 24.9 元类的实际运用

可简化或代替元类的现代功能：

- 类装饰器：比元类更易于理解，而且导致基类与元类产生冲突的可能性更小。
- `__set_name__`：无须自定义元类逻辑，就能自动设置描述符的名称。
- `__init_subclass__`：提供一种自定义类创建过程的方式，比装饰器更简单，但是复杂的类层次结构可能产生冲突。
- 内置的`dict`保留键的插入顺序：不使用`__prepare__`。

元类、类装饰器和`__init_subclass__`的用途：

- 注册子类。
- 验证子类结构。
- 把装饰器一次性应用到多个方法上。
- 序列化对象。
- 映射对象关系。
- 持久存储对象。
- 在类层级实现特殊方法。
- 实现其他语言特有的功能，例如面向方面程序设计。