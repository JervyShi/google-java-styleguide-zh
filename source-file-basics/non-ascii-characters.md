#### 2.3.3 非ASCII字符

对于剩余的非ASCII字符，是使用实际的Unicode字符(比如∞)，还是使用等价的Unicode转义符(比如\u221e)，取决于哪个能让代码更易于阅读和理解。

> > Tip: 在使用Unicode转义符或是一些实际的Unicode字符时，建议做些注释给出解释，这有助于别人阅读和理解。

例如：

    String unitAbbrev = "μs";                                 | 赞，即使没有注释也非常清晰
    String unitAbbrev = "\u03bcs"; // "μs"                    | 允许，但没有理由要这样做
    String unitAbbrev = "\u03bcs"; // Greek letter mu, "s"    | 允许，但这样做显得笨拙还容易出错
    String unitAbbrev = "\u03bcs";                            | 很糟，读者根本看不出这是什么
    return '\ufeff' + content; // byte order mark             | Good，对于非打印字符，使用转义，并在必要时写上注释

> > Tip: 永远不要由于害怕某些程序可能无法正确处理非ASCII字符而让你的代码可读性变差。当程序无法正确处理非ASCII字符时，它自然无法正确运行， 你就会去fix这些问题的了。(言下之意就是大胆去用非ASCII字符，如果真的有需要的话)
