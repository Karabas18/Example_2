# TRiTPO-lab2

# Требования к проекту
---
# Содержание
1 [Введение](#intro)
1.1 [Название продукта](#product_name)
1.2 [Назначение документа](#appointment)  
1.3 [Бизнес-требования](#business_requirements)  
1.3.1 [Исходные данные](#initial_data)  
1.3.2 [Возможности бизнеса](#business_opportunities)  
1.3.3 [Границы проекта](#project_boundary)  
1.4 [Аналоги](#analogues)  
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
3.1.1.2 [Настройка профиля зарегистрированного пользователя](#setting_up_the_profile_of_the_active_user)  
3.1.1.3 [Опрос пользователя о любимых жанрах фильмов](#user_asking)  
3.1.1.4 [Просмотр информации об отдельном фильме](#view_information_about_an_individual_movie)  
3.1.1.5 [Выход зарегистрированного пользователя из учётной записи](#active_user_change)  
3.1.1.6 [Регистрация нового пользователя после входа в приложение](#add_new_user)
3.1.1.7 [Просмотр фильма онлайн](#watch_movie)
3.1.1.8 [Скачивание фильма](#download_movie)
3.1.2 [Ограничения и исключения](#restrictions_and_exclusions)  
3.2 [Нефункциональные требования](#non-functional_requirements)  
3.2.1 [Атрибуты качества](#quality_attributes)  
3.2.1.1 [Требования к удобству использования](#requirements_for_ease_of_use)  
3.2.1.2 [Требования к безопасности](#security_requirements)  
3.2.2 [Внешние интерфейсы](#external_interfaces)  
3.2.3 [Ограничения](#restrictions)  
---


# 1 Введение
<a name="intro"/>

## 1.1 Название продукта
<a name="product_name"/>
MovieBox

## 1.2 Назначение документа
<a name="appointment"/>
В этом документе описаны функциональные и нефункциональные требования к веб-сервису «MovieBox» для ОС Windows 10.
Этот документ предназначен для команды, которая будет реализовывать и проверять корректность работы веб-сервиса.

## 1.3 Бизнес-требования
<a name="business_requirements"/>

### 1.3.1 Исходные данные
<a name="initial_data"/>
Просмотр фильмов является одним из самых распространенных видов досуга. Около 10 лет назад основными возможностями просмотра фильмов для людей
любых возрастных категорий были телевидение и кинотеатры. Однако, не всегда жанр показываемого фильма совпадает с интересами зрителя, или, может не быть возможности
посетить интересный киносеанс. С развитием технологий онлайн-кинотеатров люди получили возможность персонализировать свои интересы,
ознакамливаться с интересами других людей и выбирать фильм любого жанра и рейтинга, не заботясь о подборе времени для просмотра или фильма по интересам.
В связи с этим появляется множество интернет-приложений(сервисов), позволяющих использовать технологии просмотра и подборки фильмов онлайн.

### 1.3.2 Возможности бизнеса
<a name="business_opportunities"/>
Многие люди желают иметь веб-сервис, позволяющий просматривать фильмы любых жанров онлайн, подбирать фильмы для пользователя, основываясь на
его предпочтениях и оценках. Подобный сервис позволит им тратить меньше времени на поиск необходимой информации и использовать сервис в удобное время, 
не подстаиваясь под ТВ-расписание или прокат в кинотеатрах. Интерфейс, спроектированный с учётом всех особенностей похожих технологий, и дополнение веб-сервиса подробной инструкцией позволят увеличить количество людей, использующих данный сервис.
Подбор фильмов будет осуществляться по специальному алгоритму, учитывающему результаты анкетирования пользователя, предлагаемого веб-сервисом.

### 1.3.3 Границы проекта
<a name="project_boundary"/>
Веб-сервис "MovieBox" позволит зарегистрированным пользователям просматривать фильмы любого жанра и года выпуска онлайн, скачивать фильмы для дальнейшего просмотра
оффлайн, формировать свой рейтинг фильмов, получать подборку от пользователей с похожими оценками на фильмы и от самого приложения, основываясь на предпочтениях
пользователя и его оценках, видеть сформированный сервисом рейтинг фильмов и оставлять отзывы на фильмы на общем ресурсе. Незарегистрированным пользователям будут доступны только:просмотр рекламных роликов фильмов, просмотр оценок на фильмы и чтение отзывов

## 1.4 Аналоги
<a name="analogues"/>
«Кинопоиск" — крупнейший русскоязычный интернет-сервис о кино. С 2018 года также доступен онлайн-кинотеатр с несколькими тысячами фильмов, сериалов, мультфильмов, в том числе премьерных и эксклюзивных. Сервис позволяет просматривать фильмы и получать подборки, основываясь на предпочтениях пользователя.

Internet Movie Database (IMDb, в переводе с англ. — «Интернет-база фильмов») — веб-сайт со свободно редактируемой и крупнейшей в мире базой данных о кинематографе. По состоянию на январь 2021 года, в базе собрана информация о более чем 6,5 млн кинофильмов, телесериалов и отдельных их серий, а также о 10,4 млн персоналий, связанных с кино и телевидением, — актёрах, режиссёрах, сценаристах и других. Сервис позволяет получать любые сведения о фильмах и изучать оценки и отзывы пользователей

Netflix, Inc. — американская развлекательная компания, а также стриминговый сервис фильмов и сериалов. Cервис позволяет просматривать фильмы и получать доступ к оценкам и рецензиям.

### 1.4.1 Отличия от аналогов
В отличие от "Кинопоиска" и Netflix веб-сервис MovieBox создает подборку фильмов для просмотра, учитывая заполненную пользователем анкету;
Также, в отличие от IMDb, на веб-сервисе возможен онлайн-просмотр фильмов и их скачивание

# 2 Требования пользователя
<a name="user_requirements"/>

## 2.1 Программные интерфейсы
<a name="software_interfaces"/>
Веб-сервис использует ресурс MovieBox.dev, созданный для реализации алгоритмов поиска и подборки
Язык программирования: Java
API: Java SE, Java EE
Фреймворки: Spring, Hibernate, Play, Lombok, Java Media Framework

## 2.2 Интерфейс пользователя
<a name="user_interface"/>

Окно входа в сервис.  
![Окно входа в приложение](https://github.com/VladislavSavko/TRiTPO-lab2/blob/main/mockups/%D0%9C%D0%BE%D0%BA%D0%B0%D0%BF%20%D0%BE%D0%BA%D0%BD%D0%B0%20%D0%B2%D1%85%D0%BE%D0%B4%D0%B0%20%D0%B2%20%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5.png)

Главное окно сервиса.
![Главное окно приложения](https://github.com/VladislavSavko/TRiTPO-lab2/blob/main/mockups/%D0%9C%D0%BE%D0%BA%D0%B0%D0%BF%20%D0%B3%D0%BB%D0%B0%D0%B2%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%BE%D0%BA%D0%BD%D0%B0%20%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F.png)
 
Окно регистрации нового пользователя.
![Окно регистрации нового пользователя](https://github.com/VladislavSavko/TRiTPO-lab2/blob/main/mockups/%D0%9C%D0%BE%D0%BA%D0%B0%D0%BF%20%D0%BE%D0%BA%D0%BD%D0%B0%20%D1%80%D0%B5%D0%B3%D0%B8%D1%81%D1%82%D1%80%D0%B0%D1%86%D0%B8%D0%B8%20%D0%BD%D0%BE%D0%B2%D0%BE%D0%B3%D0%BE%20%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F.png)

Главное окно сервиса после выбора фильма.
![Главное окно приложения после выбора фильма](https://github.com/VladislavSavko/TRiTPO-lab2/blob/main/mockups/%D0%9C%D0%BE%D0%BA%D0%B0%D0%BF%20%D0%B3%D0%BB%D0%B0%D0%B2%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%BE%D0%BA%D0%BD%D0%B0%20%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%20%D0%B2%D1%8B%D0%B1%D0%BE%D1%80%D0%B0%20%D1%84%D0%B8%D0%BB%D1%8C%D0%BC%D0%B0.png)

Окно настройки профиля пользователя.
![Окно настройки профиля пользователя](https://github.com/VladislavSavko/TRiTPO-lab2/blob/main/mockups/%D0%9C%D0%BE%D0%BA%D0%B0%D0%BF%20%D0%BE%D0%BA%D0%BD%D0%B0%20%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B8%20%D0%BF%D1%80%D0%BE%D1%84%D0%B8%D0%BB%D1%8F%20%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F.png)

Окно просмотра фильма онлайн.
![Окно просмотра фильма онлайн](https://github.com/VladislavSavko/TRiTPO-lab2/blob/main/mockups/%D0%9C%D0%BE%D0%BA%D0%B0%D0%BF%20%D0%BE%D0%BA%D0%BD%D0%B0%20%D0%BF%D1%80%D0%BE%D1%81%D0%BC%D0%BE%D1%82%D1%80%D0%B0%20%D1%84%D0%B8%D0%BB%D1%8C%D0%BC%D0%BE%D0%B2.png)

## 2.3 Характеристики пользователей
<a name="user_specifications"/>

### 2.3.1 Классы пользователей
<a name="user_classes"/>
1)Зарегистрированные пользователи - пользователи, которые вошли в приложение под своим именем (псевдонимом), желающие просматривать фильмы, отобранных согласно их предпочтениям. Имеют доступ к полному функционалу
2)Анонимные пользователи - пользователи, которые не хотят регистрироваться в приложении. Имеют доступ к частичному функционалу

### 2.3.2 Аудитория приложения
<a name="application_audience"/>

#### 2.3.2.1 Целевая аудитория
<a name="target_audience"/>
Люди младшей и средней возрастной категории со средним или выше среднего уровнем образования, обладающие минимальной технической грамотностью.

#### 2.3.2.2 Побочная аудитория
<a name="collateral_audience"/>
Люди старшей возрастной аудитории, обладающие вышеперечисленными качествами

### 2.4 Предположения и зависимости
<a name="assumptions_and_dependencies"/>
1. Приложение не работает при отсутствии подключения к Интернету;
2. Приложение не обрабатывает данные фильмов, недоступных в момент запроса;
3. Качество изображения зависит от скорости подключения пользователя.

# 3 Cистемные требования
<a name="system_requirements"/>

## 3.1 Функциональные требования
<a name="functional_requirements"/>

### 3.1.1 Основные функции
<a name="main_functions"/>

#### 3.1.1.1 Вход пользователя в приложение
<a name="user_logon_to_the_application"/>
**Описание.** Пользователь имеет возможность использовать приложение без создания собственного профиля либо войдя в свою учётную запись.

| Функция | Требования | 
|:---|:---|
| Вход в приложение без создания собственного профиля | Приложение должно предоставить пользователю возможность войти в приложение анонимно |
| Регистрация нового пользователя | Приложение должно запросить у пользователя ввести имя для создания учётной записи. Пользователь должен либо ввести имя, либо отменить действие |
| *Пользователь с таким именем существует* | *Приложение должно известить пользователя об ошибке регистрации и запросить ввод псевдонима. Пользователь должен либо ввести псевдоним, либо отменить действие* |
| Вход зарегистрированного пользователя в приложение | Приложение должно предоставить пользователю список имён (псевдонимов) зарегестрированных пользователей. Пользователь должен либо выбрать из списка своё имя (псевдоним), либо отменить действие |

#### 3.1.1.2 Настройка профиля зарегистрированного пользователя
<a name="setting_up_the_profile_of_the_active_user"/>
**Описание.** Зарегистрированный пользователь имеет возможность редактировать свой профиль, с которого производится выборка фильмов

| Функция | Требования | 
|:---|:---|
| Редактирование общей информации о пользователе | Приложение должно предоставить зарегистрированному пользователю поле для ввода общей информации о себе. Пользователь должен либо ввести информацию и подвердить действие, либо отменить его |
| Редактирование информации о любимых жанрах фильмов | Зарегистрированный пользователь имеет возможножность редактировать список любимых жанров фильмов |

#### 3.1.1.3 Опрос пользователя о любимых жанрах фильмов
<a name="user_asking"/>
**Описание.** Зарегистрированный пользователь имеет возможность указать приложению свои предпочтения жанров фильмов, которые в дальнейшем обработаются приложением и используются для выборки фильмов для пользователя

| Функция | Требования | 
|:---|:---|
| Заполнение анкеты о предпочитаемых жанрах фильмов | Приложение должно предоставить зарегистрированному пользователю поле для ввода информации о предпочитаемых жанрах фильмов. Пользователь должен либо ввести информацию и подвердить действие, либо пропустить его |

#### 3.1.1.4 Просмотр информации об отдельном фильме
<a name="view_information_about_an_individual_movie"/>
**Описание.** Зарегистрированный пользователь имеет возможность просматривать краткую и полную информацию о фильме

| Функция | Требования | 
|:---|:---|
| Просмотр предварительной(краткой) информации | Приложение должно предоставить пользователю возможность увидеть краткую информацию о фильме на главной странице |
| Просмотр полной информации | Приложение должно предоставить пользователю возможность увидеть полную информацию о фильме |
| *Фильма не существует* | *Приложение должно известить пользователя об ошибке, запросить повторный ввод и показать похожие фильмы по выборке. Пользователь должен либо ввести информацию заново, либо выбрать другой фильм, либо отменить действие* |

#### 3.1.1.5 Выход зарегистрированного пользователя из учетной записи
<a name="active_user_change"/>
**Описание.** Зарегистрированный пользователь имеет возможность выйти из своего профиля и продолжить работать с приложением анонимно

**Требование.** Приложение должно предоставить зарегистрированному пользователю возможность выйти из учётной записи с возвратом к окну входа в приложение.

#### 3.1.1.6 Регистрация нового пользователя после входа в приложение
<a name="add_new_user"/>
**Описание.** Анонимный пользователь имеет возможность зарегистрироваться в приложении.

**Требование.** Приложение должно предоставить анонимному пользователю возможность [зарегистрироваться в приложении]

#### 3.1.1.7 Просмотр фильма онлайн
<a name="watch_movie"/>
**Описание.** Зарегистрированный пользователь имеет возможность просматривать фильм онлайн

**Требование.** Приложение должно предоставить анонимному пользователю возможность просмотра фильма онлайн, отобразив графический интерфейс просмотра фильма

#### 3.1.1.8 Скачивание фильма
<a name="download_movie"/>
**Описание.** Зарегистрированный пользователь имеет возможность скачать фильм на свое устройство

**Требование.** Приложение должно предоставить анонимному пользователю возможность скачивания фильма, отобразив графический интерфейс скачивания фильма

### 3.1.2 Ограничения и исключения
<a name="restrictions_and_exclusions"/>
1. Приложение работает только при наличии подключения к Интернету;
2. Приложение функционирует корректно только при корректной работе сервиса MovieBox.dev 

## 3.2 Нефункциональные требования
<a name="non-functional_requirements"/>

### 3.2.1 Атрибуты качества
<a name="quality_attributes"/>

#### 3.2.1.1 Требования к удобству использования
<a name="requirements_for_ease_of_use"/>
1. Доступ к основным функциям приложения не более чем за две операции;
2. Все функциональные элементы пользовательского интерфейса имеют названия, описывающие действие, которое произойдет при выборе элемента;
3. Пошаговая инструкция использования основных функций приложения отображена в справке;
4. Обновление информации о фильмах происходит каждые 30 минут в фоновом режиме.
5. Понятный графический интерфейс

#### 3.2.1.2 Требования к безопасности
<a name="security_requirements"/>
Приложение предоставляет возможность просмотра и редактирования профиля только активного пользователя.
Приложение гарантирует безопасность личных данных пользователей.

### 3.2.2 Внешние интерфейсы
<a name="external_interfaces"/>
Окна приложения удобны для использования пользователями с плохим зрением:
  * размер шрифта не менее 14пт;
  * функциональные элементы контрастны фону окна.

### 3.2.3 Ограничения
<a name="restrictions"/>
1. Приложение реализовано на платформе Spring Framework 5.3.1;
2. Профиль пользователя хранится в файле с расширением XML, название файла совпадает с именем (псевдонимом);
3. Информация о фильмах хранится в базе данных MySQL.
