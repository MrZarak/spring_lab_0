# Колодяжний Дмитро Сергійович ІО-01
## Лаба 0

### В чому полягає різниця між Spring Framework та Spring Boot?
Spring Framework це стандартний фреймворк для продакшин-реді розробки під Java, який містить в собі різні модулі, як ось:
1. Spring Core
2. Spring AOP
3. Spring Data
4. Spring MVC
5. Spring Security

Spring Boot — це розширення Spring'а, яке усуває бойлерплейт код по створенню дефолтних конфігурації та бінів, аналізуючи classpath, application.properties проекту.
### Для чого в структурі проекту потрібен файл pom.xml?
POM — це файл, який містить в собі інформацію про проект, його залежності, та інші метадані. Він використовується Maven'ом для збірки проекту.
### Для чого потрібна анотація @SpringBootApplication? Що буде, якщо її прибрати?
Анотація @SpringBootApplication використовується для вказівки на те, що клас є точкою входу в Spring Boot додаток. Якщо її прибрати, то Spring Boot не зможе знайти точку входу в додаток.
### Для чого потрібен інтерфейс CommandLineRunner?
CommandLineRunner — це інтерфейс, який містить в собі метод run, який викликається після запуску Spring Boot додатку. Цей інтерфейс використовується для виконання коду після запуску додатку.
### Чим інтерфейс CommandLineRunner відрізняється від ApplicationRunner?
CommandLineRunner — це інтерфейс, який містить в собі метод run, який приймає String[] args. ApplicationRunner — це інтерфейс, який містить в собі метод run, який приймає ApplicationArguments args. ApplicationArguments — це інтерфейс, який містить в собі методи для роботи з вхідними аргументами.
### Використовуючи анотацію @Component додайте в перший проект два біна First та Second з інтерфейсом CommandLineRunner, які виводять на консоль слова "First" та "Second" відповідно. За допомогою анотації @Order зробіть так, щоб рядки на консоль виводились у наступному порядку:
Зроблено
### Додайте у другий проект кілька статичних HTML-сторінок про вашу команду в цілому та кожного з вас.
Зроблено