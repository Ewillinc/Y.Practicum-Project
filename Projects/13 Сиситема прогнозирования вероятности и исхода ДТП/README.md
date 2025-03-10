## Описание проекта
### Задача:
Проверка потенциальной возможности по историческим данным создать систему, способную определять вероятность ДТП с любым повреждением транспортного средства.

* Идея находится в стадии предварительного обсуждения и проработки, без четкого алгоритма работы и похожих решений на рынке. 
* Ключевой особенностью является не создание, а проверка возможности превращения идеи в результат.
### Описание данных в database:
####  Vehicles ( Описание автомобиля)
text:

* case_id - идентификационный номер в базе данных ( категориальный)
* vehicle_type - тип кузова (категории)
* vehicle_transmission - тип коробки переключения передач ( категории)


integer:

* id - индекс текущей таблицы (категория) 
* party_number - нет подробного описания 
* vehicle_age - возраст автомобиля ( число)


#### Collisions (информация о происшествиях)
text:

* case_id - идентификационный номер в бд(категория)
* country_city_location - номер географических районов где произошло дтп ( число, категория)
* country_location - названия географических районов где произошло дтп (категория)
* distance - растояние от главно дороги( число, числительные данные)
* direction - направление движения( категория)
* weather_1 - погода (категория)
* location_type - тип дороги (категория)
* collision_damage - серьезность происшествия ( категория, в бд указан как текст)
* primary_collision_factor - основной фактор аварии ( категория )
* pcf_violation_category - категория нарушения (число, категория)
* type_of_collision - тип аварии(категория)
* motor_vehicle_involved_with - дополнительные участники дтп( категория)
* road_surface - состояние дороги ( категория)
* road_condition_1 - дорожное состояние ( категория)
* lighting - освещение ( категория) 
* control_device - устройство управления (категория)


integer:

* intersection является ли место происшествия перекрестком (категория, в бд указано как integer)
* party_count - количество учатников (число) 


time:
* collision_time - время происшествия(24 часовой формат)



date:
* collision_date - дата происшествия ( year/month/day)
#### Parties (описание участников происшествия)
text:

* case_id - идентификационный номер в базе данных (кникальная категория)
* party_type - тип участников происшествия  (категории)
* party_sobriety - трезвость участников ( категории) 
* party_drug_physical - состояние участника(физическое или с учетом принятых препаратов) (категории)


integer:

* id - индекс текущей таблицы
* party_number - номер участника происшествия( от 1 до N по числу участников происшествия)
* at_fault - виновность участника (бинарная категория)
* insurance_premium - сумма страховки ( число в $) 
* cellphone_in_use - наличие телефона в автомобиле ( бинарная категория)