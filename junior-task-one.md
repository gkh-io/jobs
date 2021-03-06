# Задача №1 на вакансию junior backend developer C#

Найдите изменения на множестве данных

## Описание

Задан тип CounterData

```c#
// Показания счетчика за месяц
class CounterData
{
    // идентификатор счетчика
    public string CounterId {get;set;}

    // год
    public int Year {get;set;}

    // месяц
    public int Month {get;set;}

    // показания
    public decimal Value {get;set;}
}
```

На вход получаем две коллекции 
`List<CounterData>` в одной из которых содержаться старые значения, в другой
новые. Необходимо определить, какие значения были изменены. 
Результат представлен в виде типа

```c#
class ComparisonResult 
{
    //удаленные данные (есть в старой коллекции, но нет в новой) 
    public List<CounterData> Deleted {get;set;}

    //добавленные данные (есть в новой коллекции, но нет в старой)
    public List<CounterData> Added {get;set;}

    //данные, которые изменились. Есть в старой и новой коллекции, но
    //отличаются значением Value
    public List<ChangedData> Changed {get;set;}
}
```

Подразумевается что входные данные могут быть до 100 000 записей. Желательно 
оптимизировать функцию по скорости.

## Платформа

dotNet любой версиии

## Формат решения

* Проект должен быть выложен на GitHub и открываться с помощьюм VS2019
* В readme.md репозитория должно быть описание того как запустить и проверить
работоспособность программы

## Сложность

Предполагается решение задачи за 1-2 часа.
