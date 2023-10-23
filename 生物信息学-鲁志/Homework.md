## 2.1 Basic Command

2. 
```
grep 'chr_' test_command.gtf | grep 'YDL248W' > YDL.gtf
```

3. 
```
sed 's/chr_/chromosome_/g' test_command.gtf | cut -f 1,3,4,5 > cut.gtf
```

4. 利用`awk`命令互换示例文件的第2列和第3列，并且对输出结果利用 sort 命令依照第4和第5列数字大小排序，将最终结果输出到result.gtf文件中

```
awk '{t = $3; $3 = $2; $2 = t; print $0}' test_command.gtf | sort -k 4 -k 5 -n > result.gtf
```

## 2.2 Practice




