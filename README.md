我曾经一次次的add,commit一直提交不了，总是在add的时候出现问题，
今天终于找到原因了。
我本来是ignore了node_modules中的文件后，提交push是成功的，哪知道
加上这个目录的内容后总是失败。
曾以为原因是文件太大了，不过百度后不是这个原因。
于是就百度git bash上面的一个提示Filename too long
原来是filename加上url太长了，就试用了这个命令：
	git config --global core.longpaths true.
然后，再进行add,commit,push
哈哈哈！畅通无阻，真是perfect!!