<html lang="en"><head>
    <meta charset="UTF-8">
    <title></title>
<style id="system" type="text/css">h1,h2,h3,h4,h5,h6,p,blockquote {    margin: 0;    padding: 0;}body {    font-family: "Helvetica Neue", Helvetica, "Hiragino Sans GB", Arial, sans-serif;    font-size: 13px;    line-height: 18px;    color: #737373;    margin: 10px 13px 10px 13px;}a {    color: #0069d6;}a:hover {    color: #0050a3;    text-decoration: none;}a img {    border: none;}p {    margin-bottom: 9px;}h1,h2,h3,h4,h5,h6 {    color: #404040;    line-height: 36px;}h1 {    margin-bottom: 18px;    font-size: 30px;}h2 {    font-size: 24px;}h3 {    font-size: 18px;}h4 {    font-size: 16px;}h5 {    font-size: 14px;}h6 {    font-size: 13px;}hr {    margin: 0 0 19px;    border: 0;    border-bottom: 1px solid #ccc;}blockquote {    padding: 13px 13px 21px 15px;    margin-bottom: 18px;    font-family:georgia,serif;    font-style: italic;}blockquote:before {    content:"C";    font-size:40px;    margin-left:-10px;    font-family:georgia,serif;    color:#eee;}blockquote p {    font-size: 14px;    font-weight: 300;    line-height: 18px;    margin-bottom: 0;    font-style: italic;}code, pre {    font-family: Monaco, Andale Mono, Courier New, monospace;}code {    background-color: #fee9cc;    color: rgba(0, 0, 0, 0.75);    padding: 1px 3px;    font-size: 12px;    -webkit-border-radius: 3px;    -moz-border-radius: 3px;    border-radius: 3px;}pre {    display: block;    padding: 14px;    margin: 0 0 18px;    line-height: 16px;    font-size: 11px;    border: 1px solid #d9d9d9;    white-space: pre-wrap;    word-wrap: break-word;}pre code {    background-color: #fff;    color:#737373;    font-size: 11px;    padding: 0;}@media screen and (min-width: 768px) {    body {        width: 748px;        margin:10px auto;    }}</style><style id="custom" type="text/css"></style></head>
<body marginheight="0"><h2>Git guide</h2>
<hr>
<pre><code>git init //把这个目录变成Git可以管理的仓库
git add README.md //文件添加到仓库
git add . //不但可以跟单一文件，还可以跟通配符，更可以跟目录。一个点就把当前目录下所有未追踪的文件全部add了 
git commit -m "first commit" //把文件提交到仓库
git remote add origin git@github.com:wangjiax9/practice.git //关联远程仓库  
git push -u origin master //把本地库的所有内容推送到远程库上</code></pre>
<ol>
<li><p><strong>git init</strong></p>
</li>
<li><p><strong>git add README.md</strong></p>
</li>
<li><p><strong>git commit -m "first commit"</strong></p>
</li>
<li><p><strong>git remote add origin git@github.com:AngryShoes/HandBook.git</strong></p>
</li>
<li><p><strong>git push -u origin master</strong></p>
</li>
</ol>
<hr>
<p>上面的步骤是上传文件的基本步骤，刚开始上传时会把不必要的文件上传过去而github又没有删除文件夹的选项
所以只能在git客户端上删除然后再提交上去：
首先进入你的master文件夹下, Git Bash Here ,打开命令窗口

</p>
<ul>
<li>$ git --help 帮助命令</li>
<li>$ git pull origin master 将远程仓库里面的项目拉下来</li>
<li>$ dir  查看有哪些文件夹</li>
<li>$ git rm -r --cached target  删除target文件夹</li>
<li>$ git commit -m '删除了target'  提交,添加操作说明</li>
<li>$ git push -u origin master 最后再将本次更改更新到github项目上去</li>
</ul>
<p>为了避免出现上面的情况可以在要上传的同级目录下创建<a href="http://blog.csdn.net/gjy211/article/details/51607347">.gitignore</a>文件
上面的笔记部分参考了下面三位大牛的博客，如果有冒犯您请及时联系我会及时处理。

</p>
<p><a href="http://www.cnblogs.com/specter45/p/github.html">用法指南</a>

</p>
<p><a href="http://blog.csdn.net/wudinaniya/article/details/77508229">删除文件</a>

</p>
<p><a href="http://blog.csdn.net/u011419965/article/details/50536937#1-强调">markdown文本编辑</a></p>
</body></html>