# Ссылка на распределение

Для того, чтобы создать новую ссылку на распределение необходимо взять ID типа распределения из url http://lk.getsystem.pro/projects/{projectId}/counters/{**leadTypeId**}

Где **leadTypeId** -  нужная строка формата UUID.

Далее этот ID необходимо необходимо вставить в ссылку&#x20;

```
https://lk.getsystem.pro/api/counters/{leadTypeId}/value
```

## Тестирование работоспособности ссылки

Для тестирования роботоспособности необходимо добавить query параметр **test** со значением true.

```
https://lk.getsystem.pro/api/counters/{leadTypeId}/value?test=true
```

В этом случае произойдет распределение лида, но в базу данных **никакие изменения записаны не будут!**

{% hint style="warning" %}
Если задать query параметр **test**, но значением указать не строку **true**, а что-либо другое, то **произойдет ошибка**!&#x20;
{% endhint %}
