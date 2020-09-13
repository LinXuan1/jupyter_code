

```python
print("Hello Python!")
```

    Hello Python!
    


```python
import this
```

    The Zen of Python, by Tim Peters
    
    Beautiful is better than ugly.
    Explicit is better than implicit.
    Simple is better than complex.
    Complex is better than complicated.
    Flat is better than nested.
    Sparse is better than dense.
    Readability counts.
    Special cases aren't special enough to break the rules.
    Although practicality beats purity.
    Errors should never pass silently.
    Unless explicitly silenced.
    In the face of ambiguity, refuse the temptation to guess.
    There should be one-- and preferably only one --obvious way to do it.
    Although that way may not be obvious at first unless you're Dutch.
    Now is better than never.
    Although never is often better than *right* now.
    If the implementation is hard to explain, it's a bad idea.
    If the implementation is easy to explain, it may be a good idea.
    Namespaces are one honking great idea -- let's do more of those!
    


```python
names = ["Bob","jack","Lily"]
print(names[1].title())
print(names[1])
names[1] = names[1].title()
print(sorted(names , reverse = True))
print(names)
```

    Jack
    jack
    ['Lily', 'Jack', 'Bob']
    ['Bob', 'Jack', 'Lily']
    


```python
city = ["Changsha","Beijing","Wuhan","Shenzhen","Chengdu"]
print(city)
print(sorted(city))
print(city)
print(sorted(city,reverse = True))
print(city)
city.reverse()
print(city)
city.reverse()
print(city)
city.sort()
print(city)
city.sort(reverse=True)
print(city)
print(len(city))
del city[0]
print(city)
```

    ['Changsha', 'Beijing', 'Wuhan', 'Shenzhen', 'Chengdu']
    ['Beijing', 'Changsha', 'Chengdu', 'Shenzhen', 'Wuhan']
    ['Changsha', 'Beijing', 'Wuhan', 'Shenzhen', 'Chengdu']
    ['Wuhan', 'Shenzhen', 'Chengdu', 'Changsha', 'Beijing']
    ['Changsha', 'Beijing', 'Wuhan', 'Shenzhen', 'Chengdu']
    ['Chengdu', 'Shenzhen', 'Wuhan', 'Beijing', 'Changsha']
    ['Changsha', 'Beijing', 'Wuhan', 'Shenzhen', 'Chengdu']
    ['Beijing', 'Changsha', 'Chengdu', 'Shenzhen', 'Wuhan']
    ['Wuhan', 'Shenzhen', 'Chengdu', 'Changsha', 'Beijing']
    5
    ['Shenzhen', 'Chengdu', 'Changsha', 'Beijing']
    


```python
animals = ["Cat","Tiger","Pig"]
for animal in animals:
    print(animal)
    print("A " + animal.lower() + " would make a great pet.\n")
print("Any of these animals would make a great pet.")
```

    Cat
    A cat would make a great pet.
    
    Tiger
    A tiger would make a great pet.
    
    Pig
    A pig would make a great pet.
    
    Any of these animals would make a great pet.
    


```python
numbers = [number ** 3 for number in range(1,11)]
print(numbers)


```

    [1, 8, 27, 64, 125, 216, 343, 512, 729, 1000]
    


```python
current_users = ["Bob","Jack","Linda","Jo","cindy"]
'''copy_current_users = []
for current_user in current_users:
    copy_current_users.append(current_user.lower())'''
copy_current_users = [current_user.lower() for current_user in current_users] #列表解析
new_users = ["jack","Vivi","Mike","Seri","CINDY"]
for new_user in new_users:
    if(new_user.lower() in copy_current_users):
        print("输入别的用户名。")
    else:
        print(new_user.title() + "没被使用。")
```

    输入别的用户名。
    Vivi没被使用。
    Mike没被使用。
    Seri没被使用。
    输入别的用户名。
    


```python
numbers = [1,2,3,4,5,6,7,8,9]
for number in numbers:
    if(number == 1):
        print("1st")
    elif(number == 2):
        print("2nd")
    elif(number == 3):
        print("3rd")
    else:
        print(str(number) + "th")
```

    1st
    2nd
    3rd
    4th
    5th
    6th
    7th
    8th
    9th
    


```python
alien = {'x':0 , 'y':0 , 'speed':'high'}
print(alien)
alien['color'] = 'red'
print(alien)
del alien['speed']
print(alien)
```

    {'x': 0, 'y': 0, 'speed': 'high'}
    {'x': 0, 'y': 0, 'speed': 'high', 'color': 'red'}
    {'x': 0, 'y': 0, 'color': 'red'}
    


```python
like_language = {
    'Sara':'C',
    'Bob':'python',
    'Baby':'ruby',
    'CINDY':'JAVA'
}
names = ['sara','bob','baby','jo','yoyo']
like_language['Mike'] = 'C++'
copy_like_language = {}
for name,language in like_language.items():
    copy_like_language[name.title()]=language.title()
for name in names:
    if(name.title() in copy_like_language.keys()):
        print("Thanks for joining.")
    else:
        print("Please join in researching.")

```

    Thanks for joining.
    Thanks for joining.
    Thanks for joining.
    Please join in researching.
    Please join in researching.
    


```python
p_1 = { 'first':'A','last':'jo','city':'Jingzhou'}
p_2 = { 'first':'B','last':'lily','city':'Changsha'}
p_3 = { 'first':'C','last':'mike','city':'Wuhan'}
people = [p_1,p_2,p_3]
for person in people:
    print('full name: ' + person['first'] + ' ' + person['last'] + '\n' + 'city: ' + person['city'] + '\n')
```

    full name: A jo
    city: Jingzhou
    
    full name: B lily
    city: Changsha
    
    full name: C mike
    city: Wuhan
    
    


```python
favorate_places = {'lily':['Shanghai','Wuhan'],
                   'cindy':['Beijing'],
                   'jo':['Chengdu','Yueyang','Xiamen']}
for name,cities in favorate_places.items():
    if(len(cities) != 1):
        print('\n' + name.title() + "'s faverate places are ")
        for city in cities:
            print(city)
    else:
        print('\n' + name.title() + "'s faverate place is " + cities[0] + '.')
    
```

    
    Lily's faverate places are 
    Shanghai
    Wuhan
    
    Cindy's faverate place is Beijing.
    
    Jo's faverate places are 
    Chengdu
    Yueyang
    Xiamen
    


```python
cities = {'Wuhan':{'country':'Zhongguo','population':'1 billion'},
          'Beihaidao':{'country':'Riben','population':'10 million'},
          'NewYork':{'country':'Meiguo','population':'100 million'}}
for city,details in cities.items():
    print(city.title() + ':\n' + details['country'] + '\n' + details['population'])
```

    Wuhan:
    Zhongguo
    1 billion
    Beihaidao:
    Riben
    10 million
    Newyork:
    Meiguo
    100 million
    


```python
sandwich_orders = ['A','B','C','D']
finished_sandwiches = []
for sandwich_order in sandwich_orders:
    print("I made your tuna sandwich.")
    finished_sandwiches.append(sandwich_order)
for finished_sandwich in finished_sandwiches:
    print(finished_sandwich)

```

    I made your tuna sandwich.
    I made your tuna sandwich.
    I made your tuna sandwich.
    I made your tuna sandwich.
    A
    B
    C
    D
    


```python
def favorate_book(book_name):
    print("One of my favorate books is " + book_name + '.')
favorate_book("Alice in Wonderland")
```

    One of my favorate books is Alice in Wonderland.
    


```python
def name(first,second,third=''):
    name = {'first':first , 'second':second}
    if third:
        name['third'] = third
    return name
person = name('A','b',10)
print(person)
```

    {'first': 'A', 'second': 'b', 'third': 10}
    


```python
def name(first,second,third=''):
    name = first + second + third
    return name
person = name('A','b','c')
print(person)
```

    Abc
    


```python
 def name(first,second,**third):
    someone = {}
    someone['first_name'] = first
    someone['second_name'] = second
    for k,v in third.items():
        someone[k] = v
    return someone
one_person = name('JACK','Jones',location = 'Changsha',year = 12)
print(one_person)
```

    {'first_name': 'JACK', 'second_name': 'Jones', 'location': 'Changsha', 'year': 12}
    


```python
"""餐厅类"""
'''巴拉巴拉'''
class Restaurant():
    def __init__(self,restaurant_name,cuisine_type):
        self.restaurant_name = restaurant_name
        self.cuisine_type = cuisine_type
        
    def describe_restaurant(self):
        print(self.restaurant_name + ' ' + self.cuisine_type)
        
    def open_restaurant(self):
        print(self.restaurant_name + " is opening.")
        
        
class IceCreamStand(Restaurant):
    def __init__(self,restaurant_name,cuisine_type):
        super().__init__(restaurant_name,cuisine_type)
        self.flavor = 'sweet'
        
    def show_flavor(self):
        print(self.flavor)
my_restaurant = Restaurant('YUHUIMIN','ZHONGCAN')
my_restaurant.describe_restaurant()
my_restaurant.open_restaurant()
my_icecream = IceCreamStand('XK','shaokao')
my_icecream.flavor = 'sour'
my_icecream.show_flavor() 
```

    YUHUIMIN ZHONGCAN
    YUHUIMIN is opening.
    sour
    


```python
class Dog():
    def __init__(self,name,year):
        self.name = name
        self.year = year
        
    def sit(self):
        print(self.name + " is sitting.")
my_dog = Dog('XK',13)
my_dog.sit()
```

    XK is sitting.
    


```python
from collections import OrderedDict
vocab = OrderedDict()
vocab['A'] = 'a'
vocab['B'] = 'b'
vocab['C'] = 'c'
for k,v in vocab.items():
    print(k + ' - ' + v)
```

    A - a
    B - b
    C - c
    


```python
from random import randint
class Die:
    def __init__(self,sides):
        self.sides = sides
        
    def roll_die(self,times):
        for i in range(1,times+1):
            x = randint(1,self.sides)
            print(x)
        print('\n')
one = Die(6)
one.roll_die(10)
two = Die(10)
two.roll_die(10)
three = Die(20)
three.roll_die(10)
```

    6
    1
    2
    6
    1
    5
    2
    2
    2
    5
    
    
    10
    3
    7
    10
    7
    4
    10
    4
    9
    5
    
    
    5
    10
    7
    14
    1
    3
    2
    20
    6
    20
    
    
    


```python
file_name = 'pi.txt'
with open(file_name) as file:
    every_line = []
    for line in file:
        every_line.append(line.rstrip())
    print(every_line)
```

    ['3.1415', '  9265', '  35']
    


```python
file_name = 'pi.txt'
with open(file_name) as file:
    lines = file.readlines()
pi_string = ''
for line in lines:
    pi_string += line.strip()
print(float(pi_string))
print(len(pi_string))
    
```


```python
file_name = 'xk.txt'
with open(file_name,'w') as file:
    file.write("XIEKANG\n")
```


```python
try:
    print(5/0)
except ZeroDivisionError:
    print("You can't divide by zero.")
```

    You can't divide by zero.
    


```python
num_1 = input("Number one is: ")
num_2 = input("Number two is: ")
try:
    sum = float(num_1) + float(num_2) 
except ValueError:
    print("输入非数字。")
else:
    print(sum)
```

    Number one is: 3
    Number two is: 方法
    输入非数字。
    


```python
import json
f_num = input("your favorate number : ")
filename = "f_num.json"
with open(filename,'w') as file:
    json.dump(f_num,file)
```

    your favorate number : 6
    


```python
import json
filename = "f_num.json"
with open(filename) as file:
    f_num = json.load(file)
print(f_num)
```

    6
    


```python
import json
filename = "fa_num.json"
try:
    with open(filename) as file:
        f_num = json.load(file)
except FileNotFoundError:
    f_num = input("your favorate number : ")
    with open(filename,'w') as file:
        json.dump(f_num,file)
else:
    print(f_num)
```

    7
    

# 嗯嗯
## 惹我
### 嗯嗯



```python

```
