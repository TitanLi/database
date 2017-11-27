#查詢選擇器

### 1.首先先進入mongo Javascript Shell

```
$mongo
```

### 2.新增測試資料\(cillection為testData\)

```
>for(var i=1;i<11;i++) db.testData.insert({id:i,name:"user"+i,age:100+i})
```

### 3.查詢全部資料

```
>db.testData.find(query)
```

![](/assets/Screenshot from 2017-11-26 20-57-03.png)

### 4.加入查詢條件

```
>db.testData.find({id:6})
```

![](/assets/Screenshot from 2017-11-26 21-01-09.png)

### 5.進階查詢

* 小於$lt

```
>db.testData.find({age:{$lt:103}})
```

![](/assets/Screenshot from 2017-11-26 21-05-15.png)

* 小於等於$lte

```
>db.testData.find({age:{$lte:103}})
```

![](/assets/Screenshot from 2017-11-26 21-07-52.png)

* 大於$gt

```
>db.testData.find({age:{$gt:103}})
```

![](/assets/Screenshot from 2017-11-26 21-10-44.png)

* 大於等於$gte

```
>db.testData.find({age:{$gte:103}})
```

![](/assets/Screenshot from 2017-11-26 21-12-37.png)

* 給定查詢範圍

```
>db.testData.find({age:{$lt:120,$gte:109}})
```

![](/assets/Screenshot from 2017-11-26 21-15-39.png)

* 傳回key的值在某些value範圍內以$in表示

```
>db.testData.find({id:{$in:[1,3]}})
```

![](/assets/Screenshot from 2017-11-26 21-19-02.png)

* 傳回key的值不在某些value範圍內以$nin表示，此種方式效能較低，需做全資料表查詢

```
>db.testData.find({id:{$nin:[1,3]}})
```

![](/assets/Screenshot from 2017-11-26 21-22-17.png)

* 不等於$ne，此種方式效能較低，需做全資料表查詢

```
>db.testData.find({id:{$ne:1}})
```

![](/assets/Screenshot from 2017-11-26 21-24-29.png)
