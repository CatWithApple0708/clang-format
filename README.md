格式化代码clang-format的使用
==========

![License MIT](https://go-shields.herokuapp.com/license-MIT-blue.png)
![Pod version](http://img.shields.io/cocoapods/v/YTKKeyValueStore.svg?style=flat)
![Platform info](http://img.shields.io/cocoapods/p/YTKKeyValueStore.svg?style=flat)

##	前言

每次在写代码写完一行或一个文件时，都要为了一些缩进、代码不整齐、空行太多等等，对于此现象，有的开发人员是避之，导致了代码写的太乱，有的开发人员则是一个一个去review自己的代码，但同时也花了一些时间在做这件事情，用clang-format可以减轻花在这上面的时间，让开发人员可以更加关注业务开发，同时让代码更加规范优雅。

##	使用步骤

1、首先用xcode Package Manager（没有安装的要先安装）安装包安装Clang Format（安装成功后会在xcode–》Edit里面查找）。

![clang-format-01](http://yaoqi-github.github.io/images/clang-format-01.png)

![clang-format-01](http://yaoqi-github.github.io/images/clang-format-02.png)


2、然后将.clang-format文件放到项目文件夹里面（和.xcodeproj同级目录）。

![clang-format-01](http://yaoqi-github.github.io/images/clang-format-03.png)

3、前两个过程做好之后，最后一步打开开发工具xcode编写代码，每次编写完之后按command+s保存时会自动格式化代码。

##	.clang-format配置

	Language: Cpp

	#If true, analyze the formatted file for the most common alignment of & and *. PointerAlignment is then used only as fallback.
	DerivePointerAlignment: false

	IndentWidth: 4

	#@[]里面两边空格，原true
	SpacesInContainerLiterals: false

	#Add a space after @property in Objective-C, i.e. use \@property (readonly) instead of \@property(readonly).
	ObjCSpaceAfterProperty: true

	#The number of characters to use for indentation of ObjC blocks.
	ObjCBlockIndentWidth: 4

	#If true, if (a) return; can be put on a single line.
	AllowShortIfStatementsOnASingleLine: true

	#If false, spaces will be removed before assignment operators.
	SpaceBeforeAssignmentOperators: true

	#Pointer and reference alignment style.
	PointerAlignment: Right

	#The maximum number of consecutive empty lines to keep.
	MaxEmptyLinesToKeep: 1

	#每行字符的长度
	ColumnLimit: 0

	#注释对齐
	AlignTrailingComments: true

	#括号后加空格
	SpaceAfterCStyleCast: true

	—
	Language: JavaScript
	# Use 100 columns for JS.
	ColumnLimit: 0
	
##	.clang-format文件

我几乎尝试了所有的可能的配置，最后整理出一个非常好用的配置文件，我把它放到了github上了，大家要是想用的话，直接从我的github上面下载下来放到项目根目录即可。

-	[.clang-format文件地址](https://github.com/yaoqi-github/clang-format)

##	结语

配置里面只是用到了一些实用的代码格式化规则，还有更多的规则如block，switch规则等等，可以在“参考文档”里面一一亲测感受一下，相信使用过clang-format的同学们肯定感觉深刻。

参考文档：http://clang.llvm.org/docs/ClangFormatStyleOptions.html
clang-format
