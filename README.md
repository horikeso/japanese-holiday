# 概要

日付から休日を判定するJavaScriptです。

# 判定順序

国民の祝日を判定⇒振替休日を判定⇒国民の休日を判定

# 使い方例

* 固定祝日
```
Holiday.getHolidayName(new Date("2015/1/1"));

"元日"
```

* 休日ではない場合
```
Holiday.getHolidayName(new Date("2015/9/1"));

""
```

* ハッピーマンデー制度
```
Holiday.getHolidayName(new Date("2015/9/21"));

"敬老の日"
```

* 国民の休日
```
Holiday.getHolidayName(new Date("2015/9/22"));

"国民の休日"
```

* 春分の日・秋分の日
```
Holiday.getHolidayName(new Date("2017/3/20"));

"春分の日"

Holiday.getHolidayName(new Date("2017/9/23"));

"秋分の日"
```

* 月曜の振替休日
```
Holiday.getHolidayName(new Date("2017/1/2"));

"振替休日"
```
* 月曜以外の振替休日
```
Holiday.getHolidayName(new Date("2020/5/6"));

"振替休日"
```