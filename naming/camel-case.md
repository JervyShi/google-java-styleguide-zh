### 5.3 驼峰式命名法(CamelCase)

[驼峰式命名法](http://zh.wikipedia.org/wiki/%E9%A7%9D%E5%B3%B0%E5%BC%8F%E5%A4%A7%E5%B0%8F%E5%AF%AB)分大驼峰式命名法(`UpperCamelCase`)和小驼峰式命名法(`lowerCamelCase`)。 有时，我们有不只一种合理的方式将一个英语词组转换成驼峰形式，如缩略语或不寻常的结构(例如"IPv6"或"iOS")。Google指定了以下的转换方案。

名字从`散文形式`(prose form)开始:

1.  把短语转换为纯ASCII码，并且移除任何单引号。例如："Müller’s algorithm"将变成"Muellers algorithm"。
2.  把这个结果切分成单词，在空格或其它标点符号(通常是连字符)处分割开。
    *   推荐：如果某个单词已经有了常用的驼峰表示形式，按它的组成将它分割开(如"AdWords"将分割成"ad words")。 需要注意的是"iOS"并不是一个真正的驼峰表示形式，因此该推荐对它并不适用。
3.  现在将所有字母都小写(包括缩写)，然后将单词的第一个字母大写：
    *   每个单词的第一个字母都大写，来得到大驼峰式命名。
    *   除了第一个单词，每个单词的第一个字母都大写，来得到小驼峰式命名。
4.  最后将所有的单词连接起来得到一个标识符。

示例：

    Prose form                Correct               Incorrect
    ------------------------------------------------------------------
    "XML HTTP request"        XmlHttpRequest        XMLHTTPRequest
    "new customer ID"         newCustomerId         newCustomerID
    "inner stopwatch"         innerStopwatch        innerStopWatch
    "supports IPv6 on iOS?"   supportsIpv6OnIos     supportsIPv6OnIOS
    "YouTube importer"        YouTubeImporter
                              YoutubeImporter*

加星号处表示可以，但不推荐。

> > Note：在英语中，某些带有连字符的单词形式不唯一。例如："nonempty"和"non-empty"都是正确的，因此方法名`checkNonempty`和`checkNonEmpty`也都是正确的。
