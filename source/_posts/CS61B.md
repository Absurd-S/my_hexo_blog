---
title: CS61B
date: 2026-09-17 18:10:32
tags: [数据结构,Java,教程]
---

## Lecture 3

### Lists

In programming languages, a list is an ordered sequence of objects, often represented by comma-separated values between square brackets.

For example: [3, 6, 9, 12, 15]

Lists support a variety of operations, depending on the whims of whoever implemented the list.

- Append an item.
- Retrieve an item by index.
- Remove an item by index or value.

### Map（映射）

本质上是一个键值对（key-value pairs）的集合。

```java
import java.util.*;

public class test {

    void main() {

        var list = new ArrayList<>(List.of(1, 2, 3, 4, 5, 6, 7, 8, 9, 10));         // 现代化写法，创建一个泛型数组列表并赋值

        List<String> L = new ArrayList<>();             // 传统写法，创建一个字符串类型的数组列表

        L.add("a");
        L.add("b");
        L.add("c");

        String[] x = new String[3];             // 创建一个字符串类型的数组

        x[0] = "a";
        x[1] = "b";
        x[2] = "c";

        Map<String, Integer> map = new HashMap<>();             // 创建一个映射

        map.put("a", 1);
        map.put("b", 2);
        map.put("c", 3);


        IO.println(L + "\n");
        IO.println(Arrays.toString(x) + "\n");
        IO.println(map + "\n");
    }
}
```

## Lecture 4

### Unit Test

### The Selection Sort Algorithm

Selection sorting a list of N items

- Find the smallest item in the list
- Move it to the front
- Selection sort the remaining N-1 items (without touching front item!)

1. **Find the smallest item in the list**

    ```java
    import java.util.*;

    public class test {
        public static String findSmallest(String[] input) {
            int compared = input[0].compareTo(input[1]);

            if (compared > 0) {
                return input[1];
            } else if (compared < 0) {
                return input[0];
            }  else {
                return "SAME!";
            }
        }

        void main() {

            var strings = new ArrayList<String>(List.of("hello", "apple"));

            String result = findSmallest(strings.toArray(new String[0]));
            IO.println(result);
        }

    }
    ```

2. **Swap**






---------

[Time Complexity]:https://www.hello-algo.com/chapter_computational_complexity/time_complexity/

[Space Complexity]:https://www.hello-algo.com/chapter_computational_complexity/space_complexity/