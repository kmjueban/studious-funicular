## Java中Calendar对日期的操作

### Calendar的调用

Calendar cal = Calendar.getInstance();

### 常用方法

//加减时间值 
* add(int field,int amount) 

//取出指定字段的值
* get(int field) 

//返回Calendar 可指定地区
* getInstance()     

//以毫秒返回时间
* getTimeInMills() 

//加减时间值，不进位
* roll(int field,boolean up)   

//设定制定字段的值
* set(int field,int value) 

//设定完整的时间
* set(year,month,day,hour,minute) 

//以毫秒指定时间
* setTimeInMillis(long millis)

### 关键字

//每月的几号
* DATE / DAY_OF_MONTH

//小时
* HOUR/HOUR_OF_DAY

//毫秒
* MILLSECOND

//分钟
* MINUTE

//月份
* MONTH

//年份
* YEAR

//时区位移
* ZONE_OFFSET


## Java中接口和抽象类的区别

#### 抽象类

* 包含抽象方法的类一定是抽象类,由abstract修饰的类一定是抽象类
* 抽象类和抽象方法必须由abstract修饰
* 抽象类可以带有抽象方法和非抽象方法
* 抽象方法必须为protected 或者public 缺省情况下为public
* 抽象类不能用来创建对象,所以抽象类是为了被继承而创建的,所以抽象类不能由private修饰,如果抽象类不被继承,那么这个类没有一点作用
* 如果子类继承抽象类,则子类必须实现抽象类的抽象方法,如果子类没有实现父类的抽象方法 那么子类也必须定义为abstract


#### 接口

* 接口中可以含有变量,但是接口的变量会隐式的定义为public static final 也只能定义为public static final 定义为private 会报错
* 接口中可以含有方法,但是接口的方法会隐式的定义为public abstract 也只能定义为public abstract 用其他关键字会报错
* 接口中所有的方法不能有具体的实现,所有的方法都应该是抽象方法
* 如果一个类实现一个接口 那么这个类必须实现接口中的所有方法


#### 抽象类与接口的区别

* 一个类只能继承一个抽象类,但却可以实现多个接口
* 抽象类可以有默认的方法实现,但接口是完全抽象的,所有方法都不能实现
* 子类继承抽象类,如果子类不是抽象类则必须实现抽象类中的所有抽象方法,子类可以使用implement实现接口,并实现接口中所有的抽象方法
* 抽象方法可以有main方法并且可以运行,但接口不可以
* 抽象类速度比接口更快,因为接口需要寻找类中的实现方法
* 抽象类可以用public/protected/default修饰,接口只能用public修饰
