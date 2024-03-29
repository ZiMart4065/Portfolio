### Проверка корректности результатов A\B теста.

## Задача:

проверить, есть ли пересечения с конкурирующим тестом и есть ли пользователи, участвующие в двух группах теста одновременно;
проверьте равномерность распределения пользователей по тестовым группам и правильность их формирования.

## Описание проекта.

Был проведен анализ данных на соответствие техническому заданию. Проведен исследовательский анализ: распределение событий на пользователя, распределение событий в выборках по дням,  изменение конверсии в воронке в выборках на разных этапах. Проверка статистической разницы долей z-критерием.

## Вывод:


- кол-во пользователей в тесте выше, чем указано в техническом задании;

- параллельно нашему тесту проводился еще один тест;

- обнаружили пересечение пользователей по тестам. Процент пользователей попавших в группу "А" равен 11%, в группу "В" 12 %. Т.к. пользователи из конкурирующего теста равномерно распределены по группам нашего теста, можно сказать, что влияние конкурирующего теста было одинаково на обе группы. Чтобы не снижать мощности теста, пользователей оставляем;

- расчитали, что основное кол-во пользователей совершали события на 1-2 день, после 7 дня кол-во событий резко уменьшается;

- выявили, что 45% пользователей, не совершили ни одного события, т.к. их удаление приведет к потере значительной части данных- принимаем решеение оставить без изменений;

- 45% пользователей не совершивших события распределены по группам не равномерно, 64% из пользователей без событий приходится на группу "B", 36% на группу "А".

- при распределении среднего кол-ва событий на пользователя, видим, что в группе "B" в среднем совершается на 10.3% меньше событий, чем в группе "A"

- во время проведения теста проходили маркетинговые компании. Т.к. маркетинговая компания в равных долях оказывает влияние на группы нашего теста и мы не наблюдаем сильного воздействия, считаем, что это не сильно исказит наши данные;

- для расчета конверсии удалили пользователей, которые не совершили ни одного события. Конверсия в группе "В" ниже чем в группе "А", условие о приросте в 10% не выполнено.


Таким образом, после внедрение улучшенной рекомендательной системы мы наблюдаем уменьшение доли по событиям просмотра карточек товара и покупок. Тест можно назвать неудачным.
