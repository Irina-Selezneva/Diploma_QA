План по автоматизации тестирования
приложения по покупке тура


Данные:

1. Карта со статусом APPROVED - № 4444 4444 4444 4441
2. Карта со статусом DECLINED - № 4444 4444 4444 4442

Перечень автоматизированных сценариев:

I. Оплата дебетовой картой: перейти на страницу ввода данных, нажав кнопку “Купить”.

Позитивный тест на ввод данных с указанием месяца, не являющегося текущим.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма отправлена. Появляется сообщение "Успешно! Операция одобрена банком!"

Позитивный тест на ввод данных с указанием текущего месяца и года.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" номер текущего месяца в цифровом формате ХХ.
в) Ввести в поле "Год" две последние цифры текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма отправлена. Появляется сообщение: "Успешно! Операция одобрена банком!"


Позитивный тест на ввод данных с указанием карты со статусом DECLINED.

а) Ввести в поле "Номер карты" номер карты со статусом DECLINED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Ошибка! Банк отказал в проведении операции!"

Негативный тест на ввод данных с указанием несуществующей карты.

а) Ввести в поле "Номер карты" номер несуществующей карты.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Ошибка! Банк отказал в проведении операции!"

Негативный тест на ввод данных с указанием карты, в номере которой меньше 16 цифр.

а) Ввести в поле "Номер карты" номер карты, в номере которой меньше 16 цифр.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверный формат"

Негативный тест на ввод данных с указанием карты, в номере которой больше 16 цифр.

а) Ввести в поле "Номер карты" номер карты, в номере которой больше 16 цифр.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Поле "Номер карты" не дает вводить количество цифр больше 16.

Негативный тест на ввод данных с указанием карты, в номере которой буквы.

а) Ввести в поле "Номер карты" буквы.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Поле "Номер карты" не дает вводить буквы.

Негативный тест на ввод данных с незаполненным полем "Номер карты".

а) Оставить поле "Номер карты" пустым.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверный формат"

Негативный тест на ввод данных с указанием несуществующего месяца.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифру 13.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверный формат"

Негативный тест на ввод данных с указанием месяца буквами.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" буквы.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Поле "Месяц" не дает вводить буквы.

Негативный тест на ввод данных с незаполненным полем "Месяц".

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Оставить поле “Месяц” пустым.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверный формат"

Негативный тест на ввод данных с указанием прошедшего года.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12.
в) Ввести в поле "Год" две последние цифры года, который прошел.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: “Истёк срок действия карты”

Негативный тест на ввод данных с указанием года, который наступит нескоро.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12.
в) Ввести в поле "Год" цифры 99.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверно указан срок действия карты"

Негативный тест на ввод данных с указанием года, состоящим из одной цифры.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12.
в) Ввести в поле "Год" цифры 5.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверный формат"

Негативный тест на ввод данных с указанием в поле “Год” буквы.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12.
в) Ввести в поле "Год" буквы.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Поле "Год" не дает вводить буквы.

Негативный тест на ввод данных с оставлением поля “Год” пустым.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12.
в) Оставить поле "Год" пустым.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверный формат"

Негативный тест на ввод данных с заполнением поля “Владелец” только именем латиницей.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" только имя латиницей
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Поле обязательно для заполнения"

Негативный тест на ввод данных с заполнением поля “Владелец” кириллицей.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" имя фамилию кириллицей.
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверный формат"

Негативный тест на ввод данных с заполнением поля “Владелец” цифрами.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" цифры.
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверный формат"

Негативный тест на ввод данных с оставлением поля “Владелец” пустым.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Оставить поле "Владелец" пустым.
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Поле обязательно для заполнения"

Негативный тест на ввод данных с заполнением поля “Владелец” очень длинным значением на латинице.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" очень длинные имя и фамилия на латинице.
д) Ввести в поле "CVC/CVV" валидное значение из трех цифр.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Не дает ввести больше 64 символов

Негативный тест на ввод данных с заполнением поля “CVC/CVV” буквами.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" буквы.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Данные не вводятся.

Негативный тест на ввод данных с заполнением поля “CVC/CVV” четырьмя цифрами.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" четыре цифры.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Вводятся только первые три цифры.

Негативный тест на ввод данных с заполнением поля “CVC/CVV” одной цифрой.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" одну цифру.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверный формат"

Негативный тест на ввод данных с заполнением поля “CVC/CVV” двумя цифрами.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Ввести в поле "CVC/CVV" две цифры.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверный формат"

Негативный тест на ввод данных с оставлением поля “CVC/CVV” пустым.

а) Ввести в поле "Номер карты" номер карты со статусом APPROVED.
б) Ввести в поле "Месяц" цифры от 01 до 12. В случае если в поле “Год” введен текущий год, месяц должен быть на один больше текущего.
в) Ввести в поле "Год" две последние цифры года не ранее текущего года.
г) Ввести в поле "Владелец" валидные имя и фамилию латиницей
д) Оставить поле "CVC/CVV" пустым.
е) Нажать кнопку “Продолжить”.

Ожидаемый результат: Форма не отправлена. Появляется сообщение: "Неверный формат".

II. Выдача кредита по данным банковской карты: перейти на страницу ввода данных, нажав кнопку “Купить в кредит”.

ПОВТОРИТЬ ВСЕ ТЕСТЫ, КАК ДЛЯ ЧАСТИ I (оплата дебетовой картой).

Перечень используемых инструментов

Windows 10, версия 1909 - одна из последних версий операционной системы от Microsoft, в которой происходит работа над проектом.

IntelliJ IDEA Community Edition - одна из наиболее востребованных интегрированных сред разработки (IDE) для создания, тестирования и анализа ПО с применением широкого набора библиотек.

Docker - программная платформа для разработки, доставки и запуска контейнерных приложений, например, необходимых в данном проекте MySQL и PostgreSQL.

Selenide - фреймворк для автоматизированного тестирования веб-приложений на основе Selenium WebDriver.

Faker - библиотека для генерации фальшивых данных.

GitHub - онлайн-платформа для хранения, управления и совместной работы над проектами с открытым исходным кодом

Allure - фреймворк для создания простых и понятных отчётов по автотестам.

Перечень и описание возможных рисков при автоматизации

- Неопытность в написании автотестов
- Новый проект

Интервальная оценка с учётом рисков в часах

Подключение окружения - 16 часов
Написание автотестов - 80 часов
Прогон автотестов - 24 часа
Summary - 16 часов

План сдачи работ: когда будут готовы автотесты, результаты их прогона

Готовность автотестов - 18.09.2023
Результаты - 22.09.2023

















