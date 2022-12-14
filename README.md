# Симулятор аттракциона *QueueToRide*

### Класс `Person`

Каждый человек, который посетил парк аттракционов, описывается классом ```Person```. 
В полях класса хранится информация об имени, фамилии посетителя и количестве билетов у него. 
Доступ к этим данным обеспечивают методы - геттеры
* Метод `isTicketsLeft()` проверяет остались ли у посетителя билеты
* Метод `decreaseTicketsN()` уменьшает количество билетов на 1

### Класс `Main`

В `main` создана очередь на аттракцион.
```java
Queue<Person> queue = new LinkedList<>(generateClients());
``` 
Очередь заполняется людьми из списка, который вам вернёт метод `generateClients()`.
При запуске программы бесконечный цикл , пока очередь не пуста, делает итерации.
На каждой итерации вынимается из очереди следующий клиент, проверяется количество имеющихся у него билетов . Если оно неотрицательно, на экран выводится сообщение вида *<Иван Фролов прокатился на аттракционе>*.
При этом у клиента уменьшается количество билетов. Если после этого у человека остались еще билеты, он добавляется в конец очереди.
