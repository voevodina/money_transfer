# Отчёт о тестировании Main.java на ОС Windows 10

## Краткое описание
Рассчет итоговой суммы вклада клиента банка после внесения им суммы на счет.

## Описание тестов
Проводилось позитивное функциональное тестирование.

## Результаты
100% не успешный тест

Итоговая сумма счета клиента, которая должна получиться при пополнении счета, не должна была быть отрицательным значением. При пополнении счета и наличии на нем средств, сумма должна быть преумножена. 

Ошибка в расчете данных возникла вероятнее всего по причине того, что в программе изначально не была предусмотрена ситуация, что сумма счета клиента превысит значение 2 147 483 647, которое является в переменной типа int граничным.

[Баг-репорт](https://github.com/voevodina/money_transfer/issues/1)

## Общие рекомендации
Необходимо внимательно следить за тем, что при пополнении счета клиента, итоговая сумма счета не должна быть меньше изначальной.
