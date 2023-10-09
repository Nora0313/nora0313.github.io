# markdown语言的使用方法
## 一、标题

# 一级
## 二级
### 三级

- - -
## 二、分割线
使用三个或以上的`-`或者`*`，且这一行只有符号

注意：不要被识别成标题，中间或前面可以加空格

- - -
* * *

## 三、斜体和粗体
使用`*`和`**`分别表示斜体和粗体

*斜体* **粗体** ***又斜又粗***

- - -
## 四、超链接和图片
写法类似，图片前面多了一个`!`

两种写法：
[第一种写法](https://github.com/Nora0313/Nora0313.github.io/)

或者

[第二种写法][1]

[1]: https://github.com/Nora0313/Nora0313.github.io/

如果是图片：
![figure1](https://ars.els-cdn.com/content/image/1-s2.0-S0923753423007615-gr1.jpg)

- - -
## 五、无序列表
使用`-`或者`+`或者`*`
前后留一行空白，可嵌套

+ 一层
    - 二层
        * 三层
            * 四层
+ 一层

- - -
## 六、有序列表
使用`1. `（点号后面有空格）表示有序列表，可嵌套
1. 一层
    1. 二层
    2. 二层
2. 一层

- - -
## 七、文字引用
用`>`表示，可以有多个`>`，表示层级更深
>第一层
>>第二层
>这样是跳不出去的
>>>还可以更深

>这样就跳出去了

- - -
## 八、行内代码块
用\`表示

`行内代码块`
很多字符需要转义，用`\`转义

## 九、代码块
使用四个空格缩进表示代码块，


    public class Helloworld
    {
        public static void main(String[] args)
        {
            System.outsprintln( "Hello, World!" );
            }
    }


或者前后加上三个\`
```
public class Helloworld
{
    public static void main(String[] args)
    {
        System.outsprintln( "Hello, World!" );
    }
}
```
