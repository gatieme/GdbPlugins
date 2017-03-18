# GdbPlugins
-------


| subtree | 描述　|
|:-------:|:-----:|
| gdbinit | https://github.com/gdbinit/Gdbinit |
| gef | https://github.com/hugsy/gef |
| peda | https://github.com/longld/peda |


本系统为gdbinit, gef, peda　等工具, 通过 `git subtree` 方式构建

使用git remote add 在A项目中添加子项目B的简称（可选）。

```cpp
语法：git remote add -f <子仓库名> <子仓库地址>

解释：其中-f意思是在添加远程仓库之后，立即执行fetch
```

使用git subtree add 在A项目中首次添加目录引用。

```cpp
语法：git subtree add --prefix=<子目录名> <子仓库名> <分支> --squash

解释：--squash意思是把subtree的改动合并成一次commit，这样就不用拉取子项目完整的历史记录。--prefix之后的=等号也可以用空格。
```

子项目B提交后，在A项目中使用git subtree pull拉取子项目B项目中的更新。


#1      gdbinit
-------

添加

```cpp
git remote  add -f gdbinit git@github.com:gdbinit/Gdbinit.git
git subtree add --prefix=gdbinit gdbinit master --squash
```

更新 
```cpp
git subtree pull --prefix=gdbinit git@github.com:gdbinit/Gdbinit.git master --squash
```

#2      gef
-------
```cpp
git remote  add -f gef git@github.com:hugsy/gef.git
git subtree add --prefix=gef gef master --squash
```

更新 
```cpp
git subtree pull --prefix=gef git@github.com:hugsy/gef.git master --squash
```

#3      peda
-------


添加　
```cpp
git remote  add -f peda git@github.com:longld/peda.git  
git subtree add --prefix=peda peda master -squash
```


更新 

```cpp
git subtree pull --prefix=peda git@github.com:longld/peda.git master --squash
```
