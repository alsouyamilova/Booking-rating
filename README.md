# Прогнозирование рейтинга отеля на Booking 
#### (соревнование на Kaggle)

**Постановка задачи**

Одна из проблем компании — это нечестные отели, которые накручивают себе рейтинг. Одним из способов обнаружения таких отелей является построение модели, которая предсказывает рейтинг отеля. Если предсказания модели сильно отличаются от фактического результата, то, возможно, отель ведёт себя нечестно, и его стоит проверить.
Поставлена задача создать такую модель.


**Данные для модели**

Датасет содержит сведения о 515 000 отзывах на отели Европы. Модель, которую предстоит обучать, должна предсказывать рейтинг отеля по данным сайта Booking на основе имеющихся в датасете данных. Набор данных разделен на 2 части: train и test. После обучения модели необходимо предсказать целевую переменную для датасета test и отправить файл submission в соревнование на Kaggle.<br>
Файлы данных доступны по [ссылке](https://drive.google.com/drive/folders/1fjCqXibx84TRcybyBo93KNT-_s5voxMd?usp=sharing) <br>

Первоначальная версия датасета содержит 17 полей со следующей информацией:

*hotel_address* — адрес отеля;
*review_date* — дата, когда рецензент разместил соответствующий отзыв;
*average_score* — средний балл отеля, рассчитанный на основе последнего комментария за последний год;
*hotel_name* — название отеля;
*reviewer_nationality* — страна рецензента;
*negative_review* — отрицательный отзыв, который рецензент дал отелю;
*review_total_negative_word_counts* — общее количество слов в отрицательном отзыв;
*positive_review* — положительный отзыв, который рецензент дал отелю;
*review_total_positive_word_counts* — общее количество слов в положительном отзыве.
*reviewer_score* — оценка, которую рецензент поставил отелю на основе своего опыта;
*total_number_of_reviews_reviewer_has_given* — количество отзывов, которые рецензенты дали в прошлом;
*total_number_of_reviews* — общее количество действительных отзывов об отеле;
*tags* — теги, которые рецензент дал отелю;
*days_since_review* — количество дней между датой проверки и датой очистки;
*additional_number_of_scoring* — есть также некоторые гости, которые просто поставили оценку сервису, но не оставили отзыв. Это число указывает, сколько там действительных оценок без проверки.
*lat* — географическая широта отеля;
*lng* — географическая долгота отеля.

**Этапы проекта**
- подгрузка и знакомство с данными
- очистка данных
- проектирование признаков
- нормализация данных
- кодирование признаков
- отбор признаков на основании корреляции и статистической значимости
- создание и обучение модели
- предсказание целевой переменной на тестовых данных
- отправка результата в соревнование на Kaggle
