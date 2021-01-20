# Лог
```
Please open 'ru.netology.JvmExperience' in VisualVm
16:46:34.209: loading io.vertx
16:46:34.592: loaded 529 classes
16:46:37.593: loading io.netty
16:46:38.389: loaded 2117 classes
16:46:41.389: loading org.springframework
16:46:41.653: loaded 869 classes
16:46:44.653: now see heap
16:46:44.653: creating 5000000 objects
16:46:46.771: created
16:46:49.773: creating 5000000 objects
16:46:49.995: created
16:46:53.011: creating 5000000 objects
16:46:57.386: created
```
## Описание

-  Загружен io.vertx (529 классов).
![](https://github.com/AndreyE-lance/netology-jvm/blob/main/images/1.jpg?raw=true)

-  Загружен io.netty (2117 классов).
![](https://github.com/AndreyE-lance/netology-jvm/blob/main/images/2.jpg?raw=true)

-  Загружен org.springframework (869 классов).
![](https://github.com/AndreyE-lance/netology-jvm/blob/main/images/3.jpg?raw=true)

-  Созданы  5000000 экземпляров класса SimpleObject. Размер Heap увеличился, количество загруженных классов выросло на 1(SimpleObject?), 
больше новых класоов загружено не будет.
![](https://github.com/AndreyE-lance/netology-jvm/blob/main/images/4.jpg?raw=true)

- Далее, будет повторятся процесс создания 5000000 экземпляров класса SimpleObject. Heap будет расти по мере приближения к критическому объему его заполнения. 
