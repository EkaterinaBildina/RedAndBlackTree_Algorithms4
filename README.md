# RedAndBlackTree_Algorithms4

Main Class
    Вызов методов и функций для создания нового дерева и работы с ним.

Node Class: 
    Конструктор атрибутов для Node.
          • нода может быть левой или правой
          • определяем значение ноды целочисленное
          • Каждая нода имеет цвет в соответствии с правилами КрасноЧерногоДерева


RedBlackTree Class: 
    Описание методов для удовлетворения условия.
          • для балансировки: левый малый поворот /goLeft/, правый малый поворот /goRight/ и смена цвета /swapColors/.
          • новая нода: всегда красная /isRed/
          • добавление ноды /add_node/
          • удаление ноды /delete/
          • поиск ноды /find/

    Красно-черное дерево имеет следующие критерии:
          • Каждая нода имеет цвет (красный или черный)
          • Корень дерева всегда черный
          • Новая нода всегда красная
          • Красные ноды могут быть только левым ребенком
          • У краной ноды все дети черного цвета

Соответственно, чтобы данные условия выполнялись,
после добавления элемента в дерево необходимо произвести балансировку,
благодаря которой все критерии выше станут валидными.
Для балансировки существует 3 операции –
левый малый поворот, правый малый поворот и смена цвета.

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
