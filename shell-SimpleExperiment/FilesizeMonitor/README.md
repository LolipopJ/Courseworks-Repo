# 文件状态查询

编写一个SHELL程序，动态检测指定文件的状态信息，当文件的大小发生改变时，给出提示信息，并继续进行检测。

## 实验内容

1. 清屏；

2. 提示用户输入要检测其状态的文件名；

3. 显示该文件的状态信息（提示：该状态信息可由命令ls –l 来得到），或找不到该文件时的错误提示；

4. 可用 `cut` 命令，或用 `sed` 或 `awk` 命令来截取状态信息中文件的大小并保存；

5. 每隔5秒钟检测一次该文件大小的信息，并与保存的文件原来的大小相比较；

6. 如果文件大小未改变，则屏幕显示不变，并继续每隔5秒钟检测一次；

7. 如果文件大小已改变，则保存新的文件大小，并在屏幕上显示：

    > file [ filename ] size changed

    括号中的 `filename` 为本程序运行时用户输入的被检测的文件名。

    程序继续每隔5秒钟检测一次文件的大小；

8. 程序循环执行5~7步的操作。当被检测的文件已累计改变了两次大小，或者已连续被检测了十次还未改变大小时，给出相应提示，然后清屏退出。