#### 4.8.5 注解(Annotations)

注解紧跟在文档块后面，应用于类、方法和构造函数，一个注解独占一行。这些换行不属于自动换行(第4.5节，自动换行)，因此缩进级别不变。例如：

    @Override
    @Nullable
    public String getNameIfPresent() { ... }

**例外**：单个的注解可以和签名的第一行出现在同一行。例如：

    @Override public int hashCode() { ... }

应用于字段的注解紧随文档块出现，应用于字段的多个注解允许与字段出现在同一行。例如：

    @Partial @Mock DataLoader loader;

参数和局部变量注解没有特定规则。


