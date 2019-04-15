1. Вкладка "перезвон". 
1.1. При checkbox on, напротив "время перезвона выбрано" отображается инпут date time, ниже отображаются варианты перезвона - "перезвонить через", для быстрого отображения этого значения в инпуте. 
1.1.1. То есть при нажатии на вариант времени перезвона, значение отображается в инпут date time, в соответствии с выбранным временем. Например если сейчас 12:00 01.01.2019 и я нажимаю на "перезвонить" через 10 минут, то значение инпут станет 12:10 01.01.2019.
1.2. Варианты "перезвонить через" соблюдая орфорграфию, запятые и переносы строк: 
	- 10 минут, 30 минут
	- 1 час, 2 часа, 3 часа
	- 1 день,   2 дня,   3 дня  
	- 1 неделя  
1.2.1. Значения выше подчеркнуты пунктиром.
1.3. Ниже располагается еще один чекбокс "отложить себе". 
1.3.1. При checkbox on появляется блок "Мои отложенные задания", который состоит из этой фразы, находящейся над таблицей, и самой таблицы. 
1.3.2. В таблице 5 столбцов.
1.3.3. В шапке: 
	- Время звонка (моё)	
	- Дата/время клиента	
	- Группа очередей	
	- Макс. балл	
	- Последний комментарий
1.3.4. Если у пользователя ранее не были отложены таски - других строк нет. 
1.3.5. Если были - они хранятся в этой таблице, по умолчанию их нет. 
1.3.6. Если пользователь ранее указал время перезвона любым способом - написав его вручную в инпут или нажав на кнопку "перезвонить через", соответственно это отложенное задание отображается в этой таблице строкой. 
1.3.7. В первом столбце помимо информации о времени звонка отображается лейбл, с синим бекграундом и его значением "новое"
1.3.8. Если я меняю время перезвона, или вношу комментарии в текст ареа выше, эти новые значение тут же отображаются в таблице.
2. Вкладка "оформление заявки". 
	Сценарий делится на 3 ветки:
	- Не готов
	- Готов предоставить квартиру под залог
	- Готов предоставить автомобиль под залог
	Они реализованы как 3 блока друг под другом каждый с radio-button, то есть переключаемся между ними, при этом, если в одном из сценариев до куда-то дошел, при выборе другого сценария, предыдущий не удаляется, и к первому можно вернуться на момент, с которого закончил.
2.1. Не готов.
	При выборе этого сценария, ниже, после блока с 3мя базовыми сценариями отображается еще блок с несколькими радио баттонами, но уже без оформления, просто списком - "причина отказа от КНЗ". Ниже неактивная кнопка "далее".
2.1.1. Варианты "причины отказа от КНЗ".
	- Не выбрано
	- Нет собственного жилья
	- Боится закладывать квартиру
	- Частный дом
	- Жилье под обременением
	- Собственники дети
	- Жилье не подходит по другим условиям
	- Нужна сумма меньше
	- Другое
	При выборе любого варианта кнопка "далее" становится активной. При нажатии на "далее" мы переходим к оформлению заявки.
2.1.1.1. Оформление заявки представляет собой форму. 
Форма разбита на несколько блоков, которые идут друг за другом.
Слева от полей формы - название поля, справа, на некоторых полях кнопка, показывающая тултип с подсказкой по полю.
ширина формы 800 px.

Названия блоков идут заголовками, с бордер-боттом в ширину формы. Равнение по левому краю.
Названия полей жирным.


	Блок: Контактные данные 
		Название поля: ФИО*. 
			Тултип: Необходимо обязательно сверять ФИО со слов Заявителя. Если данные в ФИО поменялись, внесите новые данные, убедившись, что их диктует именно Заявитель. 
		Название поля: Дата рождения*
		Название поля: Мобильный телефон*
			Тултип: Необходимо обязательно сверять номер мобильного со слов Заявителя. Вносите только личный контактный мобильный телефон Заявителя.
		Название поля: Электронная почта
			Тултип: Адрес электронной почты необходимо сверять по буквам.
	Блок: Информация о кредите наличными
		Название поля: Сумма кредита*
			Тултип: Mинимальная сумма: 50 000 р. Максимальная сумма: 2 000 000 р. Шаг: 1000 р.

2.1.1.2. После заполнения всех данных со звёздочкой кнопка "оформить заявку" становится активной.
При нажатии на неё появляется попап. Экран затемняется на 30%. В центре модальное окно 500 х 500 пикселей. 
Внутри 

- Текст
	Ориентировочный срок принятия решения по Вашей заявке и сумме кредита составляет 1-2 календарных дня. О результате рассмотрения заявки Вы будете проинформированы по SMS. Если у Вас нет ко мне вопросов, то я с Вами прощаюсь. Всего доброго, до свидания!
- Полоса с суммой баллов за задание
	Баллов за задание: 1,00, бекграунд голубой, градиентный, длинна - почти во всё модальное окно, располагается в центре, горизонтально. 
- Чекбокс "продолжить работу"
	Нижк серым "Получить задание из очереди"
- HR 
- Кнопка "Подтвердить"
- Кнопка "Отменить"
	кнопки располагаются справа. Кнопка "подтверить" синяя, "отменить" серая.

