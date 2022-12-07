# Требования к проекту
---

# Содержание
1 [Введение](#intro)  
1.1 [Назначение](#appointment)  
1.2 [Бизнес-требования](#business_requirements)  
1.2.1 [Исходные данные](#initial_data)  
1.2.2 [Возможности бизнеса](#business_opportunities)  
1.2.3 [Границы проекта](#project_boundary)  
1.3 [Обзор аналогов](#analogues)  
2 [Требования пользователя](#user_requirements)  
2.1 [Программные интерфейсы](#software_interfaces)  
2.2 [Интерфейс пользователя](#user_interface)  
2.3 [Характеристики пользователей](#user_specifications)  
2.3.1 [Классы пользователей](#user_classes)  
2.3.2 [Аудитория приложения](#application_audience)  
2.3.2.1 [Целевая аудитория](#target_audience)  
2.3.2.1 [Побочная аудитория](#collateral_audience)  
2.4 [Предположения и зависимости](#assumptions_and_dependencies)  
3 [Системные требования](#system_requirements)  
3.1 [Функциональные требования](#functional_requirements)  
3.1.1 [Основные функции](#main_functions)  
3.1.1.1 [Вход пользователя в приложение](#user_logon_to_the_application)  
3.1.1.2 [Загрузка товаров](#output_all_books)  
3.1.1.3 [Просмотр информации об отдельной позиции](#view_information)  
3.1.1.4 [Добавление новой книги](#add_book)  
3.1.1.5 [Изменение информации и удаление книги](#update_and_delete_book)  

3.1.1.6 [Взаимодействие с читателями](#write_notice_and_delete_people) 

3.1.1.7 [Темная тема](#dark_theme) 
3.1.2 [Ограничения и исключения](#restrictions_and_exclusions)  
3.2 [Нефункциональные требования](#non-functional_requirements)  
3.2.1 [Атрибуты качества](#quality_attributes)  
3.2.1.1 [Требования к удобству использования](#requirements_for_ease_of_use)  
3.2.2 [Внешние интерфейсы](#external_interfaces)  
3.2.3 [Ограничения](#restrictions)  

<a name="intro"/>

# 1 Введение

<a name="appointment"/>

## 1.1 Назначение
В этом документе описаны функциональные и нефункциональные требования к приложению «MyBooks» для ОС Android. Этот документ предназначен для команды, которая будет реализовывать и проверять корректность работы приложения. 

<a name="business_requirements"/>

## 1.2 Бизнес-требования

<a name="initial_data"/>

### 1.2.1 Исходные данные
В настоящее время электронные средства информации вытесняют бумажные, и данное приложение не исключение. Оно будет разработано с целью упростить деятельность работников библиотеки.

<a name="business_opportunities"/>

### 1.2.2 Возможности бизнеса
Данное приложение является узкоспециализированным приложением для работников библиотек. Данное приложение упростит работу, а также сократит время поиска нужных книг. Данное приложение разработано на ОС Android, что также упростит время использования. Данное приложение также может быть использовано обычными людьми, имеющими свою домашнюю библиотеку для менеджмента книг. Будет добавлена регистрация через Google Account для возможности загрузки информации в облаке.

<a name="project_boundary"/>

### 1.2.3 Границы проекта
Приложение «MyBooks» позволит всем пользователям просматривать информацию о книгах, добавлять, редактировать, сортировать, удалять и фильтровать книги. Также будет возможность добавления записей о берущих книги людей и дальнейшего их оповещения по почте. Будет добавлена темня тема.

<a name="analogues"/>

## 1.3 Обзор аналогов
Существует множество приложений и сервисов для домашеней библиотеки. Данное приложение может полностью или частично охватывать аудиторию данных приложений и сервисов,но из-за узкого направления приложения, а именно запись и оповещение людей, взявших книгу, найти среди бесплатных и условно-бесплатных не удалось.

<a name="user_requirements"/>

# 2 Требования пользователя

<a name="software_interfaces"/>

## 2.1 Программные интерфейсы
Приложение обрабатывает данные из бд FireBase FireStore. 

<a name="user_interface"/>

## 2.2 Интерфейс пользователя

Далее представлен интерфейс, разработанный совместно с дизайнером.
При входе в приложение, пользователь попадает на главный экран.
<details>
<summary>Главный экран.</summary>

![Главный экран](https://user-images.githubusercontent.com/59147112/194343860-aae1686c-90b3-4594-849a-e63ac7926d14.jpg)

</details>

При нажатии на тип товара в верхней части экрана, список товаров должен быть отфильрован в соответствии с выбранным типом и обновлён.
  <details>
<summary>Отфильтрованный главный экран.</summary>

![Отфильтрованный главный экран](https://user-images.githubusercontent.com/59147112/194344130-65d6a013-da06-41a9-839c-f890e8733110.jpg) 

</details>

При нажатии на карточку товара, пользователь попадает на экран с подробной информацией о нём. На этом фрагменте пользователь может выбрать количество товара кнопками "+" и "-", и добавить в корзину, нажав кнопку "В корзину".
 <details>
<summary>Экран подробнее.  </summary>

![Экран подробнее](https://user-images.githubusercontent.com/59147112/194345614-17a10a7d-0fea-420a-b863-0ab15aa74af0.jpg)

</details>

В нижней части главного экрана расположены две кнопки "Меню" и "Корзина". По нажатии на кнопку "Корзина" открывается экран корзины, на котором пользователь может просмотреть состав своего заказа, и сделать заказ. 
<details>
<summary>Экран корзины.  </summary>

![Экран корзины](https://user-images.githubusercontent.com/59147112/194346562-76e6dad5-2e83-406f-a199-b2443bd121a8.jpg)

</details>

Если корзина пуста, то выводится заглушка.
<details>
<summary>Пустой экран корзины. </summary>

![Пустой экран корзины](https://user-images.githubusercontent.com/59147112/194347372-14ce3d30-ae26-47e2-afbe-5d57ba21961f.jpg)  

</details>

В случае отсутствия интернета, отображается экран ошибки.
<details>
<summary>Экран ошибки. </summary>

![Экран ошибки](https://user-images.githubusercontent.com/59147112/194348319-e56c3189-f5cf-46ab-8312-93481823cd4b.jpg)

</details>

<a name="user_specifications"/>

## 2.3 Характеристики пользователей

<a name="user_classes"/>

### 2.3.1 Классы пользователей

| Класс пользователей | Описание |
|:---|:---|
| Зарегистрированные пользователи | Все пользователи, зарегистрированные через Google Account  |

<a name="application_audience"/>

### 2.3.2 Аудитория приложения

<a name="target_audience"/>

#### 2.3.2.1 Целевая аудитория
Работники библиотек, обладающие минимальной технической грамотностью.

<a name="collateral_audience"/>

#### 2.3.2.2 Побочная аудитория
Люди любой возрастной категории, обладающие вышеперечисленными качествами.

<a name="assumptions_and_dependencies"/>

## 2.4 Предположения и зависимости
1. Приложение работает при отсутствии подключения к Интернету;

<a name="system_requirements"/>

# 3 Системные требования

<a name="functional_requirements"/>

## 3.1 Функциональные требования

<a name="main_functions"/>

### 3.1.1 Основные функции

<a name="user_logon_to_the_application"/>

#### 3.1.1.1 Вход пользователя в приложение
**Описание.** Приложение требует единократной авторизации и запускается сразу на главном экране.

<a name="output_all_books"/>

#### 3.1.1.2 Вывод книг
**Описание.** После входа пользователя в приложение выводит список доступных книг.

| Функция | Требования | 
|:---|:---|
| Вывод списка книг | Приложение должно выводить список книг.|
| Фильтрация книг | Приложение должно иметь возможность фильтрации по типу: "Всё", "Фантастика", "Детектив", "Приключения", "Юмор", "Учебная", "Техника", "Поэзия", "Другое".|
| Сортировка книг | Приложение должно иметь возможность фильтрации по типу: "Название", "Автор", "Год издания", "Жанр".|

<a name="view_information"/>

#### 3.1.1.3 Просмотр информации об отдельной позиции
**Описание.** Пользователь имеет возможность просмотреть информацию о каждой книге, представленной в таблице.

| Функция | Требования | 
|:---|:---|
| Просмотр информации | Пользователь имеет возможность выбрать книгу в таблице одинарным кликом по нему. Приложение должно отобразить его название, автора, описание, год, жанр и ISBN|

<a name="add_book"/>

#### 3.1.1.4 Добавление новой книги
**Описание.** Пользователь имеет возможность добавить новую книгу.

| Функция | Требования | 
|:---|:---|
| Добавление новой книги | Пользователь имеет возможность добавить книгу в список кликом по кнопке "+" на главном экране и добавить соответствующую информацию о книге|

<a name="update_and_delete_book"/>

#### 3.1.1.5 Изменение информации и удаление книги
**Описание.** Пользователь имеет возможность изменение информации и удаление книги.

| Функция | Требования | 
|:---|:---|
| Изменение информации | Пользователь имеет возможность изменить информацию о книге, выбрав соответствующую книгу, путем нажатия на нее одним кликом. На этом фрагменте должна выводиться информация о книге, кнопки "Изменить" и " Удалить", список читателей и кнопка "Запись". Изменение новой информации происходит полсле нажатия на кнопку "Изменить". Новая информация заносится путем ввода данных вручную, при этом сохраняя старую информацию в полях для изменения. Изменение новой информации фиксируется полсле нажатия на кнопку "Сохранить". После изменения информации приложение возвращает главный экран.|
| Удаление книги | Пользователь имеет возможность изменить информацию о книге, выбрав соответствующую книгу, путем нажатия на нее одним кликом. На этом фрагменте должна выводиться информация о книге, кнопки "Изменить" и " Удалить", список читателей и кнопка "Запись". Удаление кнги происходит полсле нажатия на кнопку "Удалить", Далее должно появляться новое окно с подтревждением действия. После удаления книги приложение возвращает главный экран.|

<a name="write_notice_and_delete_people"/>

#### 3.1.1.6 Взаимодействие с читателями
**Описание.** Пользователь имеет возможность сделать запись получения книги читателем с дальнейшем взаимодействием..

| Функция | Требования | 
|:---|:---|
| Запись читателя |  Пользователь имеет возможность создать запись о читателе, взявшем книгу, выбрав соответствующую книгу, путем нажатия на нее одним кликом. На этом фрагменте должна выводиться информация о книге, кнопки "Изменить" и " Удалить", список читателей и кнопка "Запись". Новая запись происходит полсле нажатия на кнопку "Запись" в правом нижнем углу экрана. Информация о читателе, а именно ФИО и электронная почта, заносится путем ввода данных вручную, а также выбор даты получения и возврата книги. Изменение новой информации фиксируется полсле нажатия на кнопку "Сохранить". После внесения информации приложение возвращает фрагмент с информацией и списком читателей выбранной книги.|
| Отправка напоминания |  Пользователь имеет возможность отправить напоминание читателю, взявшем книгу, о возврате книги, выбрав соответствующую книгу, путем нажатия на нее одним кликом. На этом фрагменте должна выводиться информация о книге, кнопки "Изменить" и " Удалить", список читателей и кнопка "Запись". В списке читателей необходимо выбрать нужную запись одним нажатием. На данном фрагменте выводится информация о записи, кнопки "Отправить напоминание" и "Удалить". Отправка уведомления происходит путем нажатия на кнопку "Отправить напонимание", после чего пользователя переносит в окно отправки сообщения. После внесения информации приложение возвращает фрагмент с информацией о выбранной записи.|
| Удаление записи | Пользователь имеет возможность отправить напоминание читателю, взявшем книгу, о возврате книги, выбрав соответствующую книгу, путем нажатия на нее одним кликом. На этом фрагменте должна выводиться информация о книге, кнопки "Изменить" и " Удалить", список читателей и кнопка "Запись". В списке читателей необходимо выбрать нужную запись одним нажатием. На данном фрагменте выводится информация о записи, кнопки "Отправить напоминание" и "Удалить". Удаление записи происходит путем нажатия на кнопку "Удаление записи", после чего пользователя переносит на фрагмент с информацией о выбранной книге.|

<a name="dark_theme"/>

#### 3.1.1.7 Темная тема
**Описание.** Пользователь имеет возможность сменить оформеление.

| Функция | Требования | 
|:---|:---|
| Темная тема |  Пользователь имеет возможность добавить книгу в список кликом по иконке шестеренок в правом верхнем углу главного экрана, где при открытии можно изменить оформление путем нажатия на кнопку.|

<a name="restrictions_and_exclusions"/>

### 3.1.2 Ограничения и исключения
1. Приложение выгружает информацию о книгах в облако только при наличии подключения к Интернету; 

<a name="non-functional_requirements"/>

## 3.2 Нефункциональные требования

<a name="quality_attributes"/>

### 3.2.1 Атрибуты качества

<a name="requirements_for_ease_of_use"/>

#### 3.2.1.1 Требования к удобству использования
1. Доступ к основным функциям приложения не более чем за одну операции;
2. Все функциональные элементы пользовательского интерфейса имеют названия или иконки, описывающие действие, которое произойдет при выборе элемента;
3. Обновление информации о людях, берущих книгу, происходит при каждом новом запуске приложения.

<a name="security_requirements"/>

### 3.2.2 Внешние интерфейсы
Окна приложения удобны для использования пользователями с плохим зрением:
  * размер шрифта не менее 14пт;
  * функциональные элементы контрастны фону окна.

<a name="restrictions"/>

### 3.2.3 Ограничения
1. Минимальная версия android 6.0.
