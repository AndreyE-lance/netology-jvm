# Задача 1

```java
public class JvmComprehension {

    public static void main(String[] args) {
        int i = 1;                      // 1
        Object o = new Object();        // 2
        Integer ii = 2;                 // 3
        printAll(o, i, ii);             // 4
        System.out.println("finished"); // 7
    }

    private static void printAll(Object o, int i, Integer ii) {
        Integer uselessVar = 700;                   // 5
        System.out.println(o.toString() + i + ii);  // 6
    }
}

```

## Описание работы

1. ClassLoader загружает классы используемые в программе(Object, Integer etc).
1. bootstrap проверяет - не содержит ли Metaspace класс JvmComprehension, и, если нет, добавляет его туда.
1. Производится проверка байт-кода.
1. JVM вызывает метод main().
1. В стеке создается фрейм для метода main().
1. Во фрейм помещается i = 1.                                                                    // 1
1. В куче созается экземпляр класса Object, а во фрейм метода main помещается ссылка на него.    // 2
1. В куче созается экземпляр класса Integer, а во фрейм метода main помещается ссылка на него.   // 3
1. Для метода printAll() создается фрэйм в стэке, в который помещается  i = 1, а так же ссылки
   на экземпляры o и ii.                                                                         // 4 
1. Создается экземпляр класса Integer - uselessVar. Ссылка нанего помещается во фрейм метода printAll() //5
1. Результат выражения o.toString() + i + ii помещается в кучу. Создается новый фрейм для метода  
println(). В него помещается результат выражения.                                                         //6
1. Строка "finished" помещается в кучу. Создается новый фрейм для метода  
println(). В него помещается строка.                                                                //7
1. После извлечения строки из фрейма, фрейм метода main() удаляется из стека. 
