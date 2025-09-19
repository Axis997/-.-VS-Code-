# -.-VS-Code-

Работа со списками / массивами
Python
Основной контейнер: список (list).
Динамический: автоматически изменяет размер.
Операторы:
append(x) — добавить элемент в конец.
pop() — удалить последний (или по индексу).
Срезы ([start:stop:step]) позволяют легко получать подсписки.
Пример:
arr = [1, 2, 3]
arr.append(4)    # [1, 2, 3, 4]
x = arr.pop()    # вернёт 4
sub = arr[::2]   # [1, 3]

C++
Основные варианты:
Массив (int arr[10]) — фиксированный размер.
std::vector — динамический массив из STL.
Операторы:
push_back(x) — добавить элемент в конец (аналог append).
pop_back() — удалить последний элемент.
Индексация [i], но нет встроенных «срезов».
Пример:
#include <vector>
using namespace std;

vector<int> v = {1, 2, 3};
v.push_back(4);   // [1, 2, 3, 4]
v.pop_back();     // [1, 2, 3]
int x = v[0];     // 1

Java
Основные структуры:
Массив (int[] arr) — фиксированный размер.
ArrayList<Integer> — динамический список.
Операторы:
add(x) — добавить в конец.
remove(index) — удалить по индексу.
get(index) — доступ к элементу.
Пример:
import java.util.ArrayList;

ArrayList<Integer> list = new ArrayList<>();
list.add(1);
list.add(2);
list.add(3);
list.remove(1); // удалит элемент с индексом 1 → [1, 3]
int x = list.get(0); // 1

Реализация стека (LIFO)

Python
Нет отдельного класса Stack, но list и collections.deque используются как стек.
Операторы:
append(x) — push.
pop() — pop.
Пример:
stack = []
stack.append('a')
stack.append('b')
print(stack.pop())

C++
Есть std::stack в STL.
Можно использовать vector или deque как основу.
Операторы:
push(x) — push.
pop() — удалить верхний.
top() — посмотреть верхний элемент.
Пример:
#include <stack>
using namespace std;

stack<char> s;
s.push('a');
s.push('b');
char x = s.top(); // 'b'
s.pop();

Java
Есть класс Stack (java.util.Stack).
Также можно использовать Deque (ArrayDeque).
Операторы:
push(x) — push.
pop() — pop.
peek() — посмотреть верхний элемент.
Пример:
import java.util.Stack;
Stack<Character> stack = new Stack<>();
stack.push('a');
stack.push('b');
char x = stack.pop();  // b

Сходства
Все языки поддерживают добавление и удаление с конца списка (push/pop).
Везде стек реализуется по принципу LIFO.
Есть динамические контейнеры:
Python → list
C++ → vector, stack
Java → ArrayList, Stack

Отличия
Язык	Список / массив	Стек
Python	list — гибкий, поддерживает срезы	Нет отдельного класса, используют list или deque
C++	array (фикс.), vector (динамич.)	Есть std::stack, методы push, pop, top
Java	int[] (фикс.), ArrayList (динамич.)	Есть Stack и Deque, методы push, pop, peek
