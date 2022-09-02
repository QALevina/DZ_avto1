### Часть 2. JUnit4

#### Описание

JUnit4 (по сравнению с JUnit5) практически не документирован, поэтому всё, что нам доступно - это [JavaDoc](https://junit.org/junit4/javadoc/latest/index.html)'и и [FAQ](https://junit.org/junit4/faq.html).

На этом уровне, **с точки зрения пользователя**, почти всё*, что поменяется - мы подключим другую библиотеку и будем использовать аннотации из неё и assert'ы.

Ключевые аннотации (вы можете прочитать JavaDoc'и на них):
![](pic/junit4-annotations.png)

Ключевые Assert'ы (вы можете прочитать JavaDoc'и на них):
![](pic/junit4-asserts.png)


#### Что нужно сделать

Сделайте ветку junit4, в которой:

1\. Добавьте в зависимости JUnit:
```groovy
dependencies {
    testImplementation 'junit:junit:4.13'
}
test {
    useJUnit()
}
```

2\. Напишите простые автотесты (без параметризации)

#### Особенности

На этом уровне для нас поменяется всего три вещи:
1. Аннотация `@Test` должна имеет Fully Qualified Name `org.junit.Test`
2. Assert'ы расположены в классе `org.junit.Assert`
3. Класс и тестовые методы должны иметь модификатор доступа `public` (именно поэтому мы вам рекомендовали прописывать модификаторы в тестовых классах) 