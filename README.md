# telhacker

中国手机号生成神器

_       _  __ _           _

```
 _       _  __ _           _
| |_ ___| |/ _(_)_ __   __| |
| __/ _ \ | |_| | '_ \ / _  |
| ||  __/ |  _| | | | | (_| |
 \__\___|_|_| |_|_| |_|\____|
                V1.0 BY:zngeek
                mail:zngeek@pm.me
  -c string
        查询的条件，列名=值
        列说明：tel(电话)，sf(省份)，city(城市),yys(运营商{移动、联通、电信})
        多个条件用逗号分隔,值可以前后加通配符*进行模糊查询
  -o string
        保存结果文件的路径，为空则不保存
  -r string
        返回的结果列名，多个列名用逗号分隔，空或者'all'表示返回全部列
```

首先使用telfind生成对应的手机号前7位
例如：

```
telfind.exe -c "tel=150*,city=贵阳,yys=移动" -r tel -o res.txt
```

然后使用teldict根据前七位手机号的文件进行字典的生成，字典采用0-9四位枚举生成所有的手机号

```
 _       _     _ _      _
| |_ ___| | __| (_) ___| |_
| __/ _ \ |/ _  | |/ __| __|
| ||  __/ | (_| | | (__| |_
 \__\___|_|\____|_|\___|\__|
                V1.0 BY:zngeek
                mail:zngeek@pm.me
  -o string
        输出文件名
  -s string
        文件名
  -t int
        线程数量 (default 100)
```

例如：

```
teldict.exe -s res.txt -o 贵阳移动150.txt -t 2000
```

------

只编译了windows X64的程序，因为我懒~~~~

by：zngeek

mail：zngeek@pm.me
