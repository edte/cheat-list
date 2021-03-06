## 退出编辑器



| :w   | 将缓冲区写入文件，即保存修改           |
| ---- | -------------------------------------- |
| :wq  | 保存修改并退出                         |
| : x  | 保存修改并退出                         |
| :q   | 退出，如果对缓冲区进行过修改，则会提示 |
| :q!  | 强制退出，放弃修改                     |

## 查找替换



| /pattern       | 向后搜索字符串pattern                                        |
| -------------- | ------------------------------------------------------------ |
| ?pattern       | 向前搜索字符串pattern                                        |
| n              | 下一个匹配(如果是/搜索，则是向下的下一个，?搜索则是向上的下一个) |
| N              | 上一个匹配(同上)                                             |
| :%s/old/new/g  | 搜索整个文件，将所有的old替换为new                           |
| :%s/old/new/gc | 搜索整个文件，将所有的old替换为new，每次都要你确认是否替换   |

## 复制粘贴

| dd   | 删除光标所在行                                               |
| ---- | ------------------------------------------------------------ |
| dw   | 删除一个字(word)                                             |
| x    | 删除当前字符                                                 |
| X    | 删除前一个字符                                               |
| D    | 删除到行末                                                   |
| yy   | 复制一行，此命令前可跟数字，标识复制多行，如6yy，表示从当前行开始复制6行 |
| yw   | 复制一个字                                                   |
| y$   | 复制到行末                                                   |
| p    | 粘贴粘贴板的内容到当前行的下面                               |
| P    | 粘贴粘贴板的内容到当前行的上面                               |
| ]p   | 有缩进的粘贴，vim会自动调节代码的缩进                        |
| "a   | 将内容放入/存入a寄存器，可以支持多粘贴板                     |

附：比如常用的一个寄存器就是系统寄存器，名称为+，所以从系统粘贴板粘贴到vim中的命令为"+p,注意此处的+不表示操作符，二十一个寄存器。

## 移动光标

在vim中移动光标跟其他的编辑器中有很大的区别，不过一旦学会了，就会飞速的在文本中移动了。



| h,j,k,l | 上，下，左，右                                               |
| ------- | ------------------------------------------------------------ |
| ctrl-f  | 上翻一页                                                     |
| ctrl-b  | 下翻一页                                                     |
| %       | 跳到与当前括号匹配的括号处，如当前在{，则跳转到与之匹配的}处 |
| w       | 跳到下一个字首，按标点或单词分割                             |
| W       | 跳到下一个字首，长跳，如end-of-line被认为是一个字            |
| e       | 跳到下一个字尾                                               |
| E       | 跳到下一个字尾，长跳                                         |
| b       | 跳到上一个字                                                 |
| B       | 跳到上一个字，长跳                                           |
| 0       | 跳至行首，不管有无缩进，就是跳到第0个字符                    |
| ^       | 跳至行首的第一个字符                                         |
| $       | 跳至行尾                                                     |
| gg      | 跳至文件的第一行                                             |
| gd      | 跳至当前光标所在的变量的声明处                               |
| [N]G    | 跳到第N行，如0G，就等价于gg，100G就是第100行                 |
| fx      | 在当前行中找x字符，找到了就跳转至                            |
| ;       | 重复上一个f命令，而不用重复的输入fx                          |
| tx      | 与fx类似，但是只是跳转到x的前一个字符处                      |
| Fx      | 跟fx的方向相反                                               |
| ),(     | 跳转到上/下一个语句                                          |
| *       | 查找光标所在处的单词，向下查找                               |
| #       | 查找光标所在处的单词，向上查找                               |
| `.      | 跳转至上次编辑位置                                           |

### 在屏幕上移动



| H    | 移动光标到当前屏幕上最上边的一行 |
| ---- | -------------------------------- |
| M    | 移动光标到当前屏幕上中间的一行   |
| L    | 移动光标到当前屏幕上最下边的一行 |

### 书签



| ma   | 把当前位置存成标签a |
| ---- | ------------------- |
| `a   | 跳转到标签a处       |

## 编辑



| r      | 替换一个字符                               |
| ------ | ------------------------------------------ |
| J      | 将下一行和当前行连接为一行                 |
| cc     | 删除当前行并进入编辑模式                   |
| cw     | 删除当前字，并进入编辑模式                 |
| c$     | 擦除从当前位置至行末的内容，并进入编辑模式 |
| s      | 删除当前字符并进入编辑模式                 |
| S      | 删除光标所在行并进入编辑模式               |
| xp     | 交换当前字符和下一个字符                   |
| u      | 撤销                                       |
| ctrl+r | 重做                                       |
| .      | 重复上一个编辑命令                         |
| ~      | 切换大小写，当前字符                       |
| g~iw   | 切换当前字的大小写                         |
| gUiw   | 将当前字变成大写                           |
| guiw   | 将当前字变成小写                           |
| >>     | 将当前行右移一个单位                       |
| <<     | 将当前行左移一个单位(一个tab符)            |
| ==     | 自动缩进当前行                             |

## 插入模式



| i    | 从当前光标处进入插入模式             |
| ---- | ------------------------------------ |
| I    | 进入插入模式，并置光标于行首         |
| a    | 追加模式，置光标于当前光标之后       |
| A    | 追加模式，置光标于行末               |
| o    | 在当前行之下新加一行，并进入插入模式 |
| O    | 在当前行之上新加一行，并进入插入模式 |
| Esc  | 退出插入模式                         |

## 可视模式

### 标记文本

| v      | 进入可视模式，单字符模式               |
| ------ | -------------------------------------- |
| V      | 进入可视模式，行模式                   |
| ctrl+v | 进入可视模式，列模式，类似于UE的列模式 |
| o      | 跳转光标到选中块的另一个端点           |
| U      | 将选中块中的内容转成大写               |
| O      | 跳转光标到块的另一个端点               |
| aw     | 选中一个字                             |
| ab     | 选中括号中的所有内容，包括括号本身     |
| aB     | 选中{}括号中的所有内容                 |
| ib     | 选中括号中的内容，不含括号             |
| iB     | 选中{}中的内容，不含{}                 |

### 对标记进行动作



| >    | 块右移               |
| ---- | -------------------- |
| <    | 块左移               |
| y    | 复制块               |
| d    | 删除块               |
| ~    | 切换块中内容的大小写 |