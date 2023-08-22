# RedAndBlackTree_Algorithms4

Исключения в программировании и их обработка (семинары)
Урок 4. Структуры данных дерево и хэш-таблица

сдаем на любом языке программирования ссылкой на гитхаб пишем в комментарии к ДЗ
плюс вся документация по классам и методам

Упрощенный вариант - бинарное дерево с балансировкой, добавление, удалением элементов.

Необходимо превратить собранное на семинаре дерево поиска в полноценное левостороннее красно-черное дерево. И реализовать в нем метод добавления новых элементов с балансировкой.

Красно-черное дерево имеет следующие критерии:
• Каждая нода имеет цвет (красный или черный)
• Корень дерева всегда черный
• Новая нода всегда красная
• Красные ноды могут быть только левым ребенком
• У краной ноды все дети черного цвета

Соответственно, чтобы данные условия выполнялись, после добавления элемента в дерево необходимо произвести балансировку, благодаря которой все критерии выше станут валидными. Для балансировки существует 3 операции – левый малый поворот, правый малый поворот и смена цвета.

-------------------------------------------------------------------------------
TEMP CODE FROM INLINE LESSON(Python):

создание нодов, создание бинарного дерева, добавление значения, удаление значения, подсчет количества элементов.
class Node:
def init(self, value, left = None, right = None):
self.value = value
self.left = left
self.right = right

def __str__(self):
    res = f'значение нашего узла: {self.value}'
    # if self.left and self.right:
    #     res = f'значение нашего узла: {self.value}, значения левого: {self.left.value}, значение правого: {self.right.value}' 
    if self.left:
        res +=  f' значение левого: {self.left.value}'
    if self.right:
        res +=  f' значение правого: {self.right.value}'            
    return res
class Tree:
def init(self, root = None):
self.root = root

if node == None or data == node.value:              
    return node, parent        

if data > node.value:             
    return self.search(node.right, data, node)
if data < node.value:            
    return self.search(node.left, data, node)
    

def add_node(self, value):
    res = self.search(self.root, value)
    if res[0] is None:
        new_node = Node(value)
        if value > res[1].value:
            res[1].right = new_node
        else:
            res[1].left = new_node
    else:
        print('Ой все, такое значение уже есть')

# def print_tree(self):
initial_node = Node(15)

tree_1 = Tree(initial_node)

print(initial_node)
tree_1.add_node(16)
print(initial_node.right)
print(initial_node)
print(tree_1.search(initial_node, 16))
