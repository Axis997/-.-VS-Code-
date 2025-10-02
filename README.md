Задание 2 
1. Бинарная и биномиальная куча
Сходства:
В Java, Python, C++ бинарная куча поддерживается стандартными библиотеками (PriorityQueue, heapq, priority_queue).
Все три языка дают доступ к операциям: вставка (push/add), удаление минимума (poll/pop), просмотр минимума (top/peek).
Биномиальную кучу пришлось писать вручную во всех трёх, т.к. стандартной реализации нет.
Различия:
Python — самый короткий синтаксис (всего пара строк с heapq).
Java требует больше кода (new PriorityQueue<>(), методы add/poll).
C++ требует настройки шаблона для min-heap (greater<int>).
При реализации биномиальной кучи: в C++ важны указатели, в Java — классы и List, в Python — словари/списки.
Куча Фибоначчи
Сходства:
В примерах на всех языках реализация учебная (в стандартной библиотеке кучи Фибоначчи нет).
Основные операции (insert, getMin) одинаково просты по логике.
Различия:
Python использует встроенную функцию min, что делает код очень коротким.
Java применяет Collections.min() и ArrayList.
C++ требует алгоритма min_element и работы с vector.
В C++ больше «низкоуровневого» кода, а Java/Python ближе к декларативному стилю.
Хэш-таблицы
Сходства:
Все три языка используют ключ → значение (ассоциативный массив).
Поддерживаются базовые операции: добавление, поиск по ключу, удаление.
Интерфейс схож: map["a"] = 1 (C++/Python) и map.put("a",1) (Java).
Различия:
Python dict встроен прямо в язык → очень короткая запись.
Java требует явного указания дженериков (Map<String,Integer>).
В C++ используются шаблоны STL (unordered_map<string,int>).
Java/Python проще по синтаксису, C++ мощнее по скорости и гибкости.

Общий вывод
Сходства: все три языка позволяют решать задачи одинаковыми структурами данных; логика операций (вставка, поиск, минимум) одинакова.
Различия:
Python → самый короткий и простой синтаксис (удобен для обучения и прототипов).
Java → строгая типизация и многословность (удобно для больших проектов).
C++ → ближе к «железу», более сложный код, но высокая производительность и гибкость.

Приверы:
Бинарная куча / Биномиальная куча
Java (бинарная куча через стандартную PriorityQueue)
PriorityQueue<Integer> heap = new PriorityQueue<>();
heap.add(5); heap.add(1);
System.out.println(heap.poll()); // 1

Python (бинарная куча через heapq)
import heapq
heap = []
heapq.heappush(heap, 5)
heapq.heappush(heap, 1)
print(heapq.heappop(heap))  # 1

C++ (бинарная куча через priority_queue)
priority_queue<int, vector<int>, greater<int>> heap;
heap.push(5); heap.push(1);
cout << heap.top(); // 1

2. Куча Фибоначчи
Java
class FibHeap {
    List<Integer> nodes = new ArrayList<>();
    void insert(int x) { nodes.add(x); }
    int getMin() { return Collections.min(nodes); }
}

Python
class FibHeap:
    def __init__(self): self.nodes = []
    def insert(self, x): self.nodes.append(x)
    def get_min(self): return min(self.nodes)

C++
struct FibHeap {
    vector<int> nodes;
    void insert(int x) { nodes.push_back(x); }
    int getMin() { return *min_element(nodes.begin(), nodes.end()); }
};

3. Хэш-таблицы
Java (HashMap)
Map<String,Integer> map = new HashMap<>();
map.put("apple", 10);
System.out.println(map.get("apple"));

Python (dict)
table = {"apple": 10}
print(table["apple"])

C++ (unordered_map)
unordered_map<string,int> mp;
mp["apple"] = 10;
cout << mp["apple"];
