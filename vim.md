# Vim 的使用
## 模式
Vim中有许多的模式，最常用的是normal模式以及insert模式。进入Vim时默认在normal模式下，在该模式下不能进行编辑；按键盘上的i键进入insert模式，在insert模式下可以进行编辑操作。类似效果的还有I、a、A、o和O，他们的与i的不同主要体现在进入insert模式后，光标的位置不同。
|按键|      光标位置         |
| -- | -------------------- |
|i   |在当前字符的前面插入字符|
|a   |在当前字符的后面插入字符|
|I   |在当前行的行首插入字符  |
|A   |在当前行的行尾插入字符  |
|o   |在当前行的下一行新建插入字符 |
|O   |在当前行的上一行新建插入字符 |

## 快捷键
### 删除快捷键
+ x 删除当前光标下的字符

|operation|motion|
| ------ | ----- |
|d 右箭头(l) |删除右边的字符|
|d 左键头(h) |删除左边的字符|
| d 3 左键头(h) |删除左边的3个字符|
|d 上箭头(k) | 删除上面的一行|
|d 3 下箭头(j)| 删除下面的三行|
|d d          |删除(剪切)这一行|
|d w     | 删除单词（光标在单词的开始）|
|d $     | 删除光标到结尾的文本|
|d i w     | 删除单词（光标在单词的中间）|
|d i "     | 删除"中的内容|
|d 4 右箭头(l)| 删除右边四个字符|

### 复制粘贴快捷键
复制为y，粘贴为p，这两个快捷键的使用与删除(d)类似。
### 上一个单词和下一个单词

+ w 下一个单词
+ b 上一个单词

### 删除并进入insert模式

|operation|motion|
| ------ | ----- |
|c w     | 删除单词并进入insert模式（光标在单词的开始）|
|c i w     | 删除单词并进入insert模式（光标在单词的中间）|
|c i "     | 删除"中的内容并进入insert模式|
|c 4 右箭头(l)| 删除右边四个字符并计入insert模式

### 查找命令
f可以查找光标后最近的一个想要的字符

例如：fv 在本行查找光标后最近的v

f: 在本行查找光标后最近的:

## 组合命令（类似shell的管道）
y f c 复制当前光标打到字符c的全部内容


## vim 配置信息
```
let mapleader=" "
syntax on
set number
set wrap
set showcmd
set wildmenu

set hlsearch
exec "nohlsearch"
set incsearch
set ignorecase
set smartcase

noremap <LEADER><CR> :nohlsearch<CR>
```