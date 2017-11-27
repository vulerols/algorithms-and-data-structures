# Курганов Никита. ИУ8-54. Задача № 36

## Условие задачи
У преподавателя есть список заданий, каждое из который имеет тип (теория/практика), тематику и уровень сложности. Постройте алгоритм для генерации списка билетов, такой, чтобы одновременно выполнялись условия:
1) в зависимости от внешних условий состав билетов меняется;
2) билет содержит ровно 2 задачи (1 теория и 1 практика) из разных тем;
3) уровень сложности всех билетов приблизительно одинаковый.

## Как работает программа

На вход программы подается input.txt файл , в котором пользователь составляет пул вопросов, задает колличество сдающих экзамен и допустимое отличие одного билета от всех остальных по сложности. Важно понимать, что честность экзамена, то есть сложность каждого вопроса по равноценности будет сильно зависить от того, как пользователь подберет пул вопросов. Например, может выпасть сложность 34 4,  где первое числобудет сложность теор. вопроса, а последнее сложность практического вопроса. Эта комбинация является не честной, т.к сложности вопросв в билете очень сильно отличаются. Так же насколько по тому, сколько в пуле будет вопросов, будет сильно зависить повторяемость вопросов в билетов. Если вопросо в пуле мало, то будет много повторяющихся вопросов в каждом билет. 
В общем, честность экзамена и гарантированность то,что удастся составить экзамен по пулу вопросов полностью ложится на плечи тому, кто этот пул вопросов состовлял. 

Итак, программа после начала работы разбивает из пула вопросы отдельно в массив вопросов по теории и отдельно в массив по практики.
Далее на основании того, какой из двух массивов больше выбираетсся тот массив, в котором будет выбрана медиана. Медиана-это элемент  массива который находится в его середине. Отсносительно этой медианы буде выбран первый билет по сложности 

## Инструкция по пользованию программой

### Формат ввода в консоли 
python /homework.py [input file (\input.txt)] [output file (\output.txt)]

### Возможности программы

Программа позволяет рандомно сгенерировать определенное колличество билетов в соответствии с ТЗ 
Можно задавать абсолютно любые уровни сложности.
Полученые билеты отличаются на выходе друг от друга по сложности в рамках дельты различия

### Формат файла input.txt

**Первая строка файла должна иметь следующий вид:**

[кол-во билетов] [дельта в %(различие между билетами)]

*Пример команды:*

5 10

После данной команды идет обязательно пустая строка и далее список вопросов.

У вопроса есть характеристики:
* Сложность вопроса (задаётся неотрицательный диапазон до любого значения сверху)
* Тип вопроса (теоретический или практический вопрос задается 0 - если теория, 1 - если практика) 

*Формат задания вопроса:*

54
0

В репозитории прикреплен пример входного файла input.txt! 
