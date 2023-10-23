## Basic Command

`cp`

    cp old_file old_file2 # 复制文件
   
    cp -r old_folder old_folder2  # 复制文件夹，需要加上 -r

`mv` 移动

    mv old_file new_file # 重命名

`cut` 取出文件中的特定列或字符

    cut -f 4 file_name            #取出第 4 列
    
    cut -d ";" -f 2 file_name     # 以分号作为输入字段的分隔符（默认为制表符），取出第 2 列

`grep`

    grep 'CDS' file_name       #显示匹配上 'CDS' 的所有行
    
    grep -v 'CDS' file_name    #显示没有匹配上'CDS'的所有行
    
    grep -w 'gene' file_name    # 必须与整个字匹配

`sed` 编辑文件

    sed 's/a/A/g' file_name     #将文件中所有的 a 替换为 A
    
    sed -n '3,6 p' file_name    #打印第3到6行
    
    sed '2 q' file_name         #打印前2行

`awk`
1. 命令格式

awk '{print $0}' 1.txt 的意思是输出1.txt文件的所有内容
2. 分隔符
awk的默认分隔符是空格和制表符，上面的例子中，若希望把逗号去掉，则可以使用 -F 参数来指定分隔符（这里指定冒号（:）和逗号（,）同时作为分隔符。）
    awk -F ':|,' '{print $2, $4, $6}' log



>Linux 文本操作的三大神器：grep、sed、awk，各自的最佳应用场景：
>>grep：使用正则表达式搜索文本，并把匹配的行打印出来，是强大的文本搜索工具；
>>sed：用于编辑匹配到的文本，是一种流编辑器；
>>awk：能够对文本进行复杂的格式处理，是一种处理文本的语言。

`sort`排序

    sort -k 5 file_name           # 按照第 5 列排序 (ASCII码顺序, 10<2)
    sort -k 5 -n file_name        # 按照第 5 列排序 (ASCII数值顺序, 10>2)

`chmod`

    chmod 755 file_name
    
    chmod -R 755 cp_folder     # -R  修改该目录中所有文件的权限

三位数分别表示文件所有者，用户组，其他人
r 表示可读，w 表示可写，x 表示可执行

用数字表示：可读 r=4，可写 w=2，可执行 x=1

例如：755 表示文件所有者对文件具有可读、可写、可执行权限，其他用户只具有可读、可执行权限。
