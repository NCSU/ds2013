Домашно 1
==========

## Задачи ##
Решенията на задачите се предават по e-mail на адрес:

> ivan.vladimirov.ivanov@gmail.com

Решенията на всяка задача трябва да бъде под формата на архивен файл (zip или rar), който да съдържа всички .cpp и/или .h файлове необходими за решаването на съответната задача. Като алтернатива архивът може да съдържа и целият проект генериран от вашата среда за разработка, но в този случай може да се наложи да изтриете всики изпълними файлове (като .exe например) за да избегнете антивирусните системи на gmail. Самите архивни файлове се изпращат като attachment-и в mail-а. Освен решения на задачите самият mail трябва да съдържа име и факултетен номер. Успех!

За примерни задачи и техните решения (както и други материали) вижте [тук]().

### Задача 1 ###
Да се напише програма, която използва стек за да изпечата в обратен ред n числа.

**Формат на входа:**

На първият ред на стандартния вход се съдържа единствено цяло число n (0 <= n <= 1000), което указва броя на числата, които следват. Следват n цели числа ai, където -1000 <= ai <= 1000. 

**Форкмат на изхода:**

Да се изпечатат n числа на стандартния изход, като всяко число е на свой собствен ред. Изпечатаните числа трябва да са в обратен ред на числата ai, които са били прочетени.

**Примерен вход:**
```
10
1
2
3
4
5
6
7
8
9
10
```

**Примерен изход:**
```
10
9
8
7
6
5
4
3
2
1
```

### Задача 2 ###
Да се напише програма, която упражнява реализация на опашка. Програмата трябва да симулира двете стандартни операции върху опашка:

* Push value - която добавя цялото число value към края на опашката.
* Pop        - която премахва числото намиращо се в предницата на опашката.

като чете операциите от стандартния вход и пише резултатите от тях на стандартния изход. За примерна реализация на опашка вижте [тук]()

**Формат на входа:**

На първия ред на стандартния вход се съдържа единствено цяло число n (0 <= n <= 1000), което указва броя на операциите, които да се симулират. Следват n операции, за Push и Pop, като вида на операцията се определя от едно число което е или 0 (за операцията Push) или 1 (за операцията Pop). Ako операцията е Push (т.е. е зададена с код 0), то кода е последван от още едно цяло число x, където -1000 <= x <= 1000 е числото което трябва да бъде добавено към края на опашката.

**Формат на изхода:**

За всяка операция от тип Pop (т.е. операция зададена с код 1), да се изпечата на отделен ред числото, което е било премахнато в резултат на операцията. Забележка - може да се предполага, че никога няма да бъде дадена операция Pop за празна опашка.

**Примерен вход:**
```
10
0 1
0 2
0 3
0 4
1
1
0 5
1
1
1
```

**Примерен изход:**
```
1
2
3
4
5
```

### Задача 3 ###
Да се реализира опашка, като се използват два стека вместо масив. За целта предоставете реализации на методите на следния клас:

```C++
template <typename T>
class QueueWithStacks {
private:
  Stack<T>* s1;
  Stack<T>* s2;
  
public:
  QueueWithStacks(int size);
  ~QueueWithStacks();
  bool Push(const T& value);
  bool Pop(T& result);
  bool Front(T& result);
  bool IsEmpty();
};
```

Може да използвате реализацията на стек показана [тук]()

За да демонстрирате реализиранaта опашка отново решете Задача 2, но този път със новата опашка.
