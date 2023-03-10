# DS_DE_exibition  

Репозиторий с примерами характерных (завершённых) проектов по тематикам **Data Science** и **Data Engeneering**, которые, на мой взгляд, уже можно показывать людям.  

|На данный момент репозиторий представлен 3-мя проектами (описания ниже):  |
:------
| 1. [***(DE_big_data)*** *Анализ логов веб-сайта*](#1) |
| 2. [***(DS_ML)*** *Моделирование оттока клиентов оператора моб.связи*](#2) |
| 3. [***(DS_ML)*** *Машинное обучение и предобработка данных*](#3) |

*Работы в достаточной мере обезличены, но могут содержать авторские примечания. Предлагаются к ознакомлению в виде тетрадок `JN / Google_Colab` с исследованиями, кодом и комментариями. По соглашению с правообладателями публикуются без исходных и итоговых данных (датасеты, модели, исходные файлы).*  

***  

## *1. АНАЛИЗ ЛОГОВ WEB-САЙТА* <a class="anchor" id="1"></a>

**Описание файлов репозитория, относящихся к проекту:**  

* ***DE_logs_analysis_pres.html*** - презентация для ознакомления с проектом, содержит общую последовательность работ в сокращённом виде, часть кода опущена.
* Подробный ход исследования описывается в:
  - ***public_DE_logs_analysis.ipynb*** - исходный `JupyterNotebook`-файл проекта, содержащий все разделы работы, код без изъятий и комментарии к выполняемым действиям,
  - ***DE_logs_analysis.html*** - копия проекта, представленная в виде html-страницы (для удобства и скорости чтения).  

#### 1.1. Задача.

Осуществить анализ данных, создать скрипт для формирования витрин данных на основе анализа файла логов web-сайта. Разработаный скрипт витрины данных имеет содержание  в соответствии с тех.заданием ниже:  
  1. Суррогатный ключ устройства.  
  2. Название устройства.  
  3. Количество пользователей.  
  4. Доля пользователей данного устройства от общего числа пользователей.  
  5. Количество совершенных действий для данного устройства.  
  6. Доля совершенных действий с данного устройства, относительно других устройств.  
  7. Список из 5 самых популярных браузеров, используемых на данном устройстве различными пользователями, с указанием доли использования для данного браузера относительно остальных браузеров.  
  8. Количество ответов сервера, отличных от 200, на данном устройстве.  
  9. Для каждого из ответов сервера, отличных от 200, сформировать поле, в котором будет содержаться количество ответов данного типа.  

#### 1.2. Ход работы.  

Выполнение разбито на стадии в рамках **ETL**-процесса: *extract*, *transform* и *load*.
- Загрузка данных.
- **Извлечение** данных.
  - Извлечения структурированной информации с помощью методов ЯП ***python***.
- **Преобразование** данных.
  - Аггрегирование и трансформация сведенных в табличную форму данных выбранными инструментами (Базы Данных, табличные прцессоры **Pandas**/**Dusk**/**SPARK**).
- **Выгрузка** результатов.
  - Витрины данных сохраняются в подходящем для дальнейшего применения виде.
- Выводы об эффективности процесса. 
***

## *2. МОДЕЛИРОВАНИЕ ОТТОКА КЛИЕНТОВ ОПЕРАТОРА МОБ.СВЯЗИ* <a class="anchor" id="2"></a>
  
**Описание файлов репозитория, относящихся к проекту:**  

* ***DS_churn_mobile_pres.html*** - презентация для ознакомления с проектом, содержит общую последовательность работ в сокращённом виде, часть кода опущена.
* Подробный ход исследования описывается в:
  - ***public_DS_churn_mobile.ipynb*** - исходный `JupyterNotebook`-файл проекта, содержащий все разделы работы, код без изъятий и комментарии к выполняемым действиям,  
  - ***DS_churn_mobile.html*** - копия проекта, представленная в виде html-страницы (для удобства и скорости чтения).  

#### 2.1. Задача.

Оператор моб.связи  **\*\*\*\*\***  хочет прогнозировать отток клиентов с помощью машинного обучения. Для чего предполагается использовать предоставленные оператором обезличенные данные об активности некоторых клиентов, информации об их тарифах и договорах.  Данные представлены в табличном виде, информация содержится в:

|.csv-файлы проекта|
:---
|`contract.csv` — информация о договоре|
|`personal.csv` — персональные данные клиента|
|`internet.csv` — информация об интернет-услугах|
|`phone.csv` — информация об услугах телефонии|

#### 2.2. Ход работы.  

Исследование разбивается на следующие этапы:

- **Декомпозиция задачи.**
    * Определение целей иследования и типа задачи (регрессия, классификация).
    * Предобработка и исследовательский анализ данных (**EDA**), поиска взаимосвязей в данных и оценка значимости признаков.
    * Подготовка выборки, исправление ошибок, обогащение данных с пом. синтеза признаков.
    * Разметка данных при необходимости выделения целевого признака.
- **Выбор моделей и метрик.**
    * Выделение признаков и целевого признака, формирование обучающей и тестовой выборок.
    * Обработка значений для машинного обучения (масштабирование и кодирование).
    * Выбор моделей для машинного обучения.
    * Выбор меры для сравнения эффективности обучения моделей. Выбор метрики для оценки модели пользователем.
- **Обучение моделей.**
    * Обучение различных ML-моделей. Настройка гиперпараметров. Проверка на наличие утечек данных.
    * Сравнение полученных результатов для выбора наилучшей модели. Получение оценок на кросс-валидации.
- **Выбор наилучшей модели.**
    * Получение оценки эфективности на тестовой выборке.
    * Обоснование выбора с использованием рабочей и бизнес-метрик.
***

## *3. МАШИННОЕ ОБУЧЕНИЕ И ПРЕДОБРАБОТКА ДАННЫХ* <a class="anchor" id="3"></a>
  
**Описание файлов репозитория, относящихся к проекту:**  

* Подробный ход исследования описывается в:
  - ***public_DS_features_selection&ML.ipynb*** - исходный `JupyterNotebook`-файл проекта, содержащий все разделы работы, код без изъятий и комментарии к выполняемым действиям,  
  - ***DS_features_selection&ML.html*** - копия проекта, представленная в виде html-страницы (для удобства и скорости чтения).  

#### 3.1. Задача.

В данной работе на примере одной из задач машинного обучения рассматривались различные способы: предобработки данных, отбора и анализа признаков, уменьшения размерности признакового пространства, подготовки данных перед их подачей в модель и популярные алгоритмы машинного обучения. Подход не претендует на полноту, носит демонстративный характер для иллюстрации определённой стадии развития проф. навыков автора.  

Источник данных (kaggle loan defaulter dataset): https://www.kaggle.com/datasets/gauravduttakiit/loan-defaulter/application_data.csv)

#### 3.2. Ход работы.  

Исследование разбивается на следующие этапы:

- **Загрузка данных. Декомпозиция задачи.**
    * Определение целей иследования и типа задачи (регрессия, классификация).
- **Предобработка данных.**
    * Предобработка (пропуски, дубликаты, ошибки).
    * Исследовательский анализ данных (**EDA**), поиск взаимосвязей и оценка значимости признаков.
    * Анализ данных для сокращения признакового пространства. Отбор признаков.  
    * Снижение размерности для визуализации данных.  
- **Обучение моделей классификации.**
    * Выбор моделей и метрик.
    * Выделение признаков и целевого признака, формирование обучающей и тестовой выборок.
    * Обработка значений для машинного обучения (масштабирование, кодирование). Создание подходящих конвейеров, трансформеров и Pipeline.
    * Выбор моделей для машинного обучения.
- **Обучение моделей.**
    * Обучение различных ML-моделей. Настройка гиперпараметров. Проверка на наличие утечек данных.
    * Сравнение полученных результатов для выбора наилучшей модели. Выбор наилучшей модели.  
- **Выбор наилучшей модели.**
    * Получение оценки эфективности на тестовой выборке.
    * Рассмотрение некоторых альтернатив и компромиссов.
    * Обоснование выбора с использованием рабочей и бизнес-метрик.  
    * Выводы.
