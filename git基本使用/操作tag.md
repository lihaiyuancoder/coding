<!--
 * @Description: 
 * @Autor: lihaiyuan
 * @Email: lihaiyuan@goldenfintech.com.cn
 * @Date: 2020-01-13 15:57:02
 -->
 tag
 如果标签打错了,可以删除
 $ git tag -d  标签名称
 因为创建的标签都只存储在本地，不会自动推送到远程。所以，打错的标签可以在本地安全删除。
 将标签推送到远程
 $ git push origin tagname
或者，一次性推送全部尚未推送到远程的本地标签：
$ git push origin --tags
如果标签已经推送到远程，要删除远程标签就麻烦一点，先从本地删除：
$ git tag -d tagname 
然后，从远程删除。删除命令也是push，但是格式如下：
$ git push origin :refs/tags/tagname
要看看是否真的从远程库删除了标签，可以登陆GitHub查看。


小结
命令git push origin <tagname>可以推送一个本地标签；

命令git push origin --tags可以推送全部未推送过的本地标签；

命令git tag -d <tagname>可以删除一个本地标签；

命令git push origin :refs/tags/<tagname>可以删除一个远程标签。

