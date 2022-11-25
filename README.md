# Колодяжний Дмитро Сергійович ІО-01

## Лаба 1

## Завдання 1

Поясніть значення наступних термінів:

- Inversion of Control (IoC);
- IoC container;
- Dependency Injection (DI);
- Dependency inversion principle.

## Відповідь

#### Inversion of Control (IoC)

Це принцип програмування, в якому об'єкти не створюються або не віддаються іншим об'єктам, але отримуються від спеціальної сутності, яка називається контейнером
впорядкування (IoC container). Він відповідає за життєвий цикл об'єктів і виконує їх впорядкування.

#### IoC container

Це об'єкт, який виконує впорядкування об'єктів і контролює їх життєвий цикл. Контейнер впорядкування використовується для впорядкування об'єктів, а також для
виконання внедрення залежностей.

#### Dependency Injection (DI)

Це процес передачі залежностей об'єкту. Залежності - це інші об'єкти, які об'єкт потребує для своєї роботи. Ці залежності передаються об'єкту через конструктор
або встановлюються в публічні поля. Це дозволяє відокремити логіку об'єкта від конкретних залежностей, які він використовує.

#### Dependency inversion principle

Це принцип програмування, який вимагає того, щоб залежності об'єкта визначалися від абстракцій, а не від конкретних класів. Це дозволяє використовувати різні
реалізації абстракцій, що зменшує залежність коду від конкретних реалізацій. Це дозволяє легше виконувати тестування, а також замінювати реалізації абстракцій в
процесі розробки.

## Завдання 2

В чому полягає різниця між анотаціями @Component та @Bean? Опишіть переваги та недоліки створення бінів за допомогою цих анотацій.

## Відповідь

#### @Component

Це анотація, яка вказує, що клас є компонентом Spring. Компоненти автоматично зареєстровані в контексті, і вони можуть бути використані як залежності. Ця
анотація використовується для визначення бінів.

#### @Bean

Це анотація, яка використовується для визначення бінів. Ця анотація використовується в класі конфігурації, щоб визначити бін. Вона може бути використана для
створення бінів, які не можуть бути створені за допомогою анотації @Component, наприклад, бінів, які використовують інші біни в своїй кастомній конфігурації.

## Завдання 3

Чому слід уникати ін’єкцій залежностей напряму у поле біна?

## Відповідь

Тому що це порушує принцип інверсії залежностей. Якщо залежності ін'єктуються напряму в поля класу, то вони стають жорсткими залежностями. Це означає, що клас
не може бути використаний в іншому контексті, якщо він використовує інші класи. Це робить код менш гнучким та незалежним від контексту.

## Завдання 4

В яких випадках краще використовувати ін’єкції залежностей за допомогою конструкторів, а в яких за допомогою сетерів?

## Відповідь
Краще використовувати ін'єкції залежностей за допомогою конструкторів, якщо клас має багато залежностей, або якщо вони є обов'язковими для створення біна. Якщо ж
клас має лише одну залежність, або ця залежність не є обов'язковою для створення біна, то краще використовувати ін'єкції залежностей за допомогою сетерів. Це
зроблено для полегшення читання коду.

## Завдання 5

В яких випадках краще використовувати біни типу singleton, а в яких prototype?

## Відповідь
Краще використовувати біни типу singleton, якщо вони є незмінними, або єдиними в системі. Краще використовувати біни типу prototype, якщо вони є змінними, або
не єдиними в системі.
## Завдання 6

Чи можливе у Spring Framework створення циркулярних залежностей при ін’єкціях?

## Відповідь
Ні, Spring Framework не підтримує циркулярні залежності. Якщо вони виявляються, то Spring Framework викине виняток BeanCurrentlyInCreationException. Це
зроблено для полегшення дебагування. Але є обхід через @Lazy аноташку

## Завдання 7

Чи може бути в одному проекті кілька класів з реалізацією якогось інтерфейсу, якщо цей інтерфейс використовується для ін’єкції залежностей?

## Відповідь
Так, може. Spring Framework знайде бін, який відповідає інтерфейсу, і використовуватиме його для ін'єкції залежностей. Якщо ж бінів, які відповідають інтерфейсу,
більше, ніж один, то Spring Framework викине виняток NoUniqueBeanDefinitionException. Це зроблено для полегшення дебагування. Якщо ж ви хочете використати
бін, який відповідає інтерфейсу, але ви хочете якийсь конкретний, то використовуйте анотацію @Qualifier.
## Завдання 8

Чи може бін мати кілька методів, помічених анотацією @Autowired?

## Відповідь
Так, може. Він буде мати кілька залежностей, які будуть ін'єктитись відповідно до типу полів.

## Завдання 9

Чи може бін мати кілька конструкторів, помічених анотацією @Autowired?

Так, може. Він буде мати кілька залежностей, які будуть ін'єктитись відповідно до типу параметрів конструктора і полів методу.