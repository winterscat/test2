---
date created: 2022-06-10
date modified: 2022-07-20
tags: dataview 
---



## dataview日历视图

```dataview
CALENDAR file.ctime
FROM ""
```

## DailyNote
```dataview
list
from "Calendar/Daily notes" and -#MOC and -#readme说明 and -#index索引 
sort dates desc
limit 999
```