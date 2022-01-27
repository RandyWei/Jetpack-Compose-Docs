
## Text 文本显示控件

```kotlin
@Composable
fun Text(
    text: String?,
    modifier: Modifier? = Modifier,
    color: Color? = Color.Unspecified,
    fontSize: TextUnit? = TextUnit.Unspecified,
    fontStyle: FontStyle? = null,
    fontWeight: FontWeight? = null,
    fontFamily: FontFamily? = null,
    letterSpacing: TextUnit? = TextUnit.Unspecified,
    textDecoration: TextDecoration? = null,
    textAlign: TextAlign? = null,
    lineHeight: TextUnit? = TextUnit.Unspecified,
    overflow: TextOverflow? = TextOverflow.Clip,
    softWrap: Boolean? = true,
    maxLines: Int? = Int.MAX_VALUE,
    onTextLayout: ((TextLayoutResult) -> Unit)? = {},
    style: TextStyle? = LocalTextStyle.current
): Unit

```

### 用法

直接显示

```kotlin
@Composable
fun TextSample() {
    Text(text = "Hello World!")
}
```

从 res 中读取文字显示

```kotlin
@Composable
fun TextSample() {
    Text(text = stringResource(R.string.content))
}
```

```xml
<resources>
    <string name="content">你好，世界!</string>
</resources>
```
### 参数

#### 设置字体颜色 

```kotlin
@Composable
fun TextSample() {
    Text(text = "Hello World!", color = Color.Red)
}
```
![Text](../assets/text1.png)