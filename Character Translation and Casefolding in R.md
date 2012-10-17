Character Translation and Casefolding in R����R�е��ַ�ת���ʹ�Сдת��
========================================================

### �������
* ��R��ʹ���У��п���֮ǰ������ַ������������ĸ���ߵߵ���˳�����ĸ���������һ�࣬һ��һ�����ܻ������Щ��ʱ������R����chartr()�������Խ�����������⡣
* ����ʱ������ʱ��������һЩ���ݿ��������������������ĸ�Ǵ�д����������ĸ��Сд�ģ��е�ʱ��Ϊ��ͳһ����������ϣ��������ȫת����Сд����ȫת���ɴ�д����R��Ҳ�ṩ�˶�Ӧ�ĺ�����

> ���º���ȫ����Դ��base���С�

### ��������;�Ͳ���
* chartr(old,new,x),���ǽ�x����Ҫ��������ĸд��old�У�����������ĸд��new�У��Ϳ��Խ�x�е���ĸ���ٵ�����������
* tolower(x)���ǽ�x�еĴ�д�ĳ�Сд��Сд��ĸ����;
* toupper(x)���ǽ�x�е�Сд�ĳɴ�д����д��ĸ���䣻
* casefold(x,upper = FALSE)���ǽ�������������ͨ��һ��������ʵ���ˣ���upper = T��ʱ�������ȫ��Ϊ��д��ĸ����֮ΪСд��ĸ��Ĭ�ϵ�Ϊ���Сд��ĸ��

### ʵ������
�����������ַ���"MiXeD cAsE 123"������������iҪ����Ϊw��X����Ϊh��s����Ϊy,Ȼ���ٴ�Сдͳһ��ʽ���Ϳ������²�����

```r
# ��������ֻ�����ַ�
x <- "MiXeD cAsE 123"
# ������ĸ
x
```

```
## [1] "MiXeD cAsE 123"
```

```r
chartr("iXs", "why", x)
```

```
## [1] "MwheD cAyE 123"
```

```r

tolower(x)
```

```
## [1] "mixed case 123"
```

```r
toupper(x)
```

```
## [1] "MIXED CASE 123"
```

```r
casefold(x, upper = FALSE)
```

```
## [1] "mixed case 123"
```

```r
casefold(x, upper = TRUE)
```

```
## [1] "MIXED CASE 123"
```

�����Ҫ��������ĸ����ĸ����λ���ǰ��ŵģ��Ϳ����ü򻯵���ʽ����ɸ�����



```r
y = "abondon relaX"
# ��Ҫ��a-D,b-E,c-F,X-w
y
```

```
## [1] "abondon relaX"
```

```r
chartr("a-cX", "D-Fw", y)
```

```
## [1] "DEondon relDw"
```


