#### 3.3.3 顺序和间距

import语句可分为以下几组，按照这个顺序，每组由一个空行分隔：

1.  所有的静态导入独立成组
2.  `com.google` imports(仅当这个源文件是在`com.google`包下)
3.  第三方的包。每个顶级包为一组，字典序。例如：android, com, junit, org, sun
4.  `java` imports
5.  `javax` imports

组内不空行，按字典序排列。
