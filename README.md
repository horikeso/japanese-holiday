# JapaneseHoliday

日付から祝日を判定する

- [GitHub Pages](https://horikeso.github.io/japanese-holiday/)

- [Demo](https://horikeso.github.io/japanese-holiday/demo.html)

## Usage

- html

```html
<script src="main.js" type="module"></script>
```

- main.js

```js
import { JapaneseHoliday } from "./japanese-holiday.js";

// for browser
window.JapaneseHoliday = JapaneseHoliday;
```

---

- 固定祝日

```js
JapaneseHoliday.getHolidayName(new Date("2015/1/1"));
```

```
"元日"
```

- ハッピーマンデー制度

```js
JapaneseHoliday.getHolidayName(new Date("2015/9/21"));
```

```
"敬老の日"
```

- 国民の休日

```js
JapaneseHoliday.getHolidayName(new Date("2015/9/22"));
```

```
"国民の休日"
```

- 春分の日・秋分の日

```js
JapaneseHoliday.getHolidayName(new Date("2017/3/20"));
```

```
"春分の日"
```

```js
JapaneseHoliday.getHolidayName(new Date("2017/9/23"));
```

```
"秋分の日"
```

- 月曜の振替休日

```js
JapaneseHoliday.getHolidayName(new Date("2017/1/2"));
```

```
"振替休日"
```

- 月曜以外の振替休日

```js
JapaneseHoliday.getHolidayName(new Date("2020/5/6"));
```

```
"振替休日"
```

- 休日以外は空文字

```js
JapaneseHoliday.getHolidayName(new Date("2015/9/1"));
```

```
""
```

# Link

[国民の祝日について - 内閣府](https://www8.cao.go.jp/chosei/shukujitsu/gaiyou.html)
