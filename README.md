# DS_DE_exibition  

Репозиторий с примерами характерных проектов (завершённых) по тематикам **Data Science** и **Data Engeneering**, которые, на мой взгляд, уже можно показывать людям.  
  
*Работы в достаточной для восприятия мере обезличены, но могут содержать авторские примечания. Предлагаются к ознакомлению в виде тетрадок `JN / Google_Colab` с соотв. исследованиями и подробными комментариями к ходу выполнения, но без исходных и итоговых данных (датасеты, модели, исходные файлы) по соглашению с правообладателями.*  
  
|На данный момент репозиторий представлен 2-мя проектами (описания ниже):  |
:------
| 1. ***(DE_big_data)*** *анализ логов веб-сайта* |
| 2. ***(DS_ML)***  *построение модели оттока клиентов оператора моб.связи* |
  
***  

|  **1. (DE_big_data) *АНАЛИЗ ЛОГОВ WEB-САЙТА***  |  **2. (DS_ML) *ПОСТРОЕНИЕ МОДЕЛИ ОТТОКА
КЛИЕНТОВ ОПЕРАТОРА МОБ.СВЯЗИ***  |
|  :---:  |  :---:  |

**Описание файлов репозитория, относящихся к проекту:**  

* ***DE_logs_analysis.html*** - презентация для ознакомления с проектом, содержит общую последовательность работ в сокращённом виде, часть кода опущена.  

* Подробный ход исследования описывается в:
  - ***DE_logs_analysis.ipynb*** - исходный `JupyterNotebook`-файл проекта, содержащий все разделы работы, код без изъятий и комментарии к выполняемым действиям,  
  - ***DE_logs_analysis.html*** - копия проекта, представленная в виде html-страницы (для удобства и скорости чтения).  

#### 1.1. Задача.

Осуществить анализ данных, создать скрипт для формирования витрин данных на основе анализа логов web-сайта. Разработаный скрипт витрины данных имеет содержание  в соответствии с заданием ниже:  

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
    *Состоит в обработке файла логов с помощью методов ЯП ***python*** для извлечения структурированной информации.*
- **Преобразование** данных.  
    *Состоит в аггрегировании и трансформации сведенных в табличную форму данных выбранными для этого инструментами и в соотв. библиотеках (Базы Данных, табличные прцессоры **Pandas**/**Dusk**/**SPARK**).*  
- **Выгрузка** результатов.  
    *Сформированные в результате работы скрипта витрины данных сохраняются в подходящем для дальнейшего применения виде.*  
- Выводы об эффективности процесса.  


## 2. (DS_ML) *ПОСТРОЕНИЕ МОДЕЛИ ОТТОКА КЛИЕНТОВ ОПЕРАТОРА МОБ.СВЯЗИ*  
  
**Описание файлов репозитория, относящихся к проекту:**  

* ***DS_churn_mobile.html*** - презентация для ознакомления с проектом, содержит общую последовательность работ в сокращённом виде, часть кода опущена.  

* Подробный ход исследования описывается в:
  - ***DS_churn_mobile.ipynb*** - исходный `JupyterNotebook`-файл проекта, содержащий все разделы работы, код без изъятий и комментарии к выполняемым действиям,  
  - ***DS_churn_mobile.html*** - копия проекта, представленная в виде html-страницы (для удобства и скорости чтения).  

#### 2.1. Задача.

Осуществить анализ данных, создать скрипт для формирования витрин данных на основе анализа логов web-сайта. Разработаный скрипт витрины данных имеет содержание  в соответствии с заданием ниже:  

  1. Суррогатный ключ устройства.  
  2. Название устройства.  
  3. Количество пользователей.  
  4. Доля пользователей данного устройства от общего числа пользователей.  
  5. Количество совершенных действий для данного устройства.  
  6. Доля совершенных действий с данного устройства, относительно других устройств.  
  7. Список из 5 самых популярных браузеров, используемых на данном устройстве различными пользователями, с указанием доли использования для данного браузера относительно остальных браузеров.  
  8. Количество ответов сервера, отличных от 200, на данном устройстве.  
  9. Для каждого из ответов сервера, отличных от 200, сформировать поле, в котором будет содержаться количество ответов данного типа.  

#### 2.2. Ход работы.  

Выполнение разбито на стадии в рамках **ETL**-процесса: *extract*, *transform* и *load*.

- Загрузка данных.  
- **Извлечение** данных.  
    *Состоит в обработке файла логов с помощью методов ЯП ***python*** для извлечения структурированной информации.*
- **Преобразование** данных.  
    *Состоит в аггрегировании и трансформации сведенных в табличную форму данных выбранными для этого инструментами и в соотв. библиотеках (Базы Данных, табличные прцессоры **Pandas**/**Dusk**/**SPARK**).*  
- **Выгрузка** результатов.  
    *Сформированные в результате работы скрипта витрины данных сохраняются в подходящем для дальнейшего применения виде.*  
- Выводы об эффективности процесса.
