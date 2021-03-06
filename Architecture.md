# Часть 1
## 1.    Тип приложения
Веб-приложение – веб-приложения для выполнения преимущественно на сервере.
## 2.    Стратегия развёртывания 
Нераспределенное развертывание.
## 3. Выбор технологии
  - Java – самый распространенный язык для веб-сервисов. Преимущества – простота применения, независимость от платформы и встроенные функции.
  - JSP – большой набор фреймворков, инструментов, IDE для любых нужд, объектно-ориентированный подход к написанию кода, строго типизированный язык, большое количество готовых решений и библиотек, низкая стоимость поддержки приложения.
  - JDBC - позволяет устанавливать соединение с базой данных согласно специально описанному URL. Драйверы могут загружаться во время работы программы динамически. Легкая в использовании технология, не требует знания низкоуровневых деталей работы с памятью и соединениями и в то же время обладает не меньшей мощью, чем, скажем, клиент доступа к серверу БД, написанный на языке C++. Многие современные драйверы JDBC не только поддерживают работу со структурированными типами данных SQL 99, но и допускают сохранение в таблицах БД целых объектов Java, а также работу с информацией, сохраняемой в обычных файлах вместо привычных таблиц.
  - Apache Tomcat - контейнер сервлетов с открытым исходным кодом. Реализует спецификацию сервлетов, спецификацию JSP и JavaServer Faces(JSF). Tomcat позволяет запускать веб-приложения, содержит ряд программ для самоконфигурирования.  
  - CSS, HTML - необходимый инструментарий для верстки и оформления веб-страниц.  
  - Bootstrap - современные библиотеки для красивого оформления сайтов и адаптивной верстки.
## 4. Показатели качества
  - Актуальность;
  - Надежность;
  - Безопасность;
  - Удобство использования.
## 5.  Пути реализации сквозной функциональности: 
- Аутентификация: обеспечить безопасность при входе путем использования только post-запросов и хэширования паролей;
- Авторизация: защита ресурсов посредством авторизации вызывающей стороны;
- Валидация - проверка всех вводимых данных;  
- Хэширование: применить алгоритм MD-2, который позволяет шифровать пароли.  
## 6. Архитектура "To Be":
Диаграмма развертывания. 
![To Be](././Image/toBe.png)
 # Часть 2
 ## Архитектура "As Is":
Диаграмма развертывания. 
![As Is](././Image/asIs.png)
 # Часть 3
 ### Проблема
 Основной проблемой текущей реализации является отсутствие уровня сервисов, что приводит к перегруженности уровня контроллера. При этом данный уровень должен являться лишь прослойкой между уровнем логики и уровнем представления. Причиной возникновения данной проблемы является ошибка на этапе проектирования. 
 ### Решение
 Реализация уровня сервисов позволит улучшить расширяемость функционала приложения. Таким образом, для добавления нового функционала не придется переписывать имеющийся код, а достаточно будет просто добавить еще один сервис.
