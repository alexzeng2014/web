<h1 id="学会atom的基础">学会Atom的基础</h1>
<p><img src="http://7xvup9.com1.z0.glb.clouddn.com/imgbgcp1.png" alt="学会Atom基础"></p>
<h2 id="目录">目录</h2>
<ul>
<li>Markdown简明语法</li>
<li>学会将Atom中的项目发送到github</li>
<li>如何修改快捷键</li>
<li>如何本地化安装插件</li>
<li>将代码显示到浏览器里面去</li>
<li>代码提示，自动提醒插件</li>
<li>任务列表：Toggle Markdown Task</li>
<li>补全路径插件 Autocomplete Paths</li>
<li>Atom 备份插件</li>
<li>代码格式化atom-beautify</li>
<li>选择高亮插件 Highlight Selected</li>
<li>Todo 查询</li>
<li>linter代码检查</li>
</ul>
<h3 id="todo">TODO</h3>
<p>在TODO加入关键词的，未完成功能的功能方便以后</p>
<h3 id="linter代码检查">linter代码检查</h3>
<p>一口气装上了两个linter-jshint和linter-scss-lint，<br>
linter-spell-html发生错误。</p>
<h3 id="simplified-chinese-menu中文菜单">simplified-chinese-menu中文菜单</h3>
<h3 id="代码格式化atom-beautify">代码格式化atom-beautify</h3>
<pre><code>'atom-text-editor:not([mini])':
  'ctrl-shift-m': 'unset!',
 'ctrl-alt-b': 'atom-beautify:beautify-editor'
</code></pre>
<h2 id="atom-备份插件">Atom 备份插件</h2>
<p>sync-settings可以同步Atom的设置文件,自定义快捷键,用户风格,初始化脚本及代码片段,还支持已安装的插件同步。绝对神器！！</p>
<ol>
<li>进入设置中心找到该插件,进去setting</li>
<li>打开自己的github创建一个personal access token – 然后复制生成的token序列,粘贴到插件的setting里面的(42ba555f6f2008e8063707c8d394105eef9c8140)</li>
<li>再打开github的gist服务,创建一个gist–复制生成gistID（3f89fe827603e169e9e58ca73fe94902）,也粘贴到二步设置里面</li>
<li>在文档编辑页面,按下全局命令搜索面板(Ctrl+shift+p) 搜索sync- ,会有可选项</li>
</ol>
<pre><code>sync-settings:backup – 这条命令是备份当前的配置
sync-settings:restore – 这条命令是回复配置,是直接覆盖的;
sync-settings:view-backup – 这条是当你执行备份后到线上查询你的备份的,也就是到你的gist code里面
sync-settings:check-backup – 这条是查询最后一次是否正常
</code></pre>
<h2 id="补全路径插件-autocomplete-paths">补全路径插件 Autocomplete Paths</h2>
<h2 id="toggle-markdown-task">Toggle Markdown Task</h2>
<p>安装Toggle Markdown Task，建立一个基于Markdown文档的Todo列表。</p>
<pre><code>- [ ] 任务类别：

Clrd+d 打勾

keymaps 文件中：

'atom-workspace atom-text-editor:not(.mini)':
  'ctrl-d': 'toggle-markdown-task:toggle'
&lt;&lt;&lt;&lt;&lt;&lt;&lt; HEAD
</code></pre>
<h2 id="md-writer让写md文档更方便">md-writer让写MD文档更方便</h2>
<p>这插件用起来相当方便，可是记住快捷键以及设置快捷键也并不是很容易的事。</p>
<p><kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>p</kbd>输入wr:然后查找也许是个不错的选择。</p>
<p>但无论如何，下面的简明语法一定得要学会。</p>
<h2 id="markdown简明语法">Markdown简明语法</h2>
<p>=======</p>
<pre><code>

### Markdown简明语法
mdown在Atom应用起来简直爽快，利用快捷键 **Ctrl+Shift+M** 可以同步浏览，而且界面巨爽！！！
&gt;&gt;&gt;&gt;&gt;&gt;&gt; origin/master

mdown在Atom应用起来简直爽快，利用快捷键 **Ctrl+Shift+M** 可以同步浏览，而且界面巨爽！！！

```
标题：
#h1级标题
##h2级标题
###h3级标题
####h4级标题
#####h5级标题
######h6级标题

分割线：三个以上的短线 即可作出分割线

----

超链接：[连接名称](网址 , 标题)
[我是链接名](http://www.izhangbo.cn, "我是标题")
[&lt;i class="icon-refresh"&gt;&lt;/i&gt; 点我刷新](/sonfilename/)

另一种超链接写法：[链接名][链接代号]
[here][3]
然后在别的地方定义 3 这个详细链接信息，
[3]: http://www.izhangbo.cn "聚牛团队"

直接展示链接的写法：&lt;http://www.izhangbo.cn&gt;

键盘键
&lt;kbd&gt;Ctrl+[&lt;/kbd&gt; and &lt;kbd&gt;Ctrl+]&lt;/kbd&gt;

code格式：反引号
Use the `printf()` function.

``There is a literal backtick (`) here.针对在代码区段内插入反引号的情况``

强调：
*斜体强调*
**粗体强调**

图片
![Alt text](http://www.izhangbo.cn/wp-content/themes/minty/img/logo.png "Optional title")

使用 icon 图标文字
&lt;i class="icon-cog"&gt;&lt;/i&gt;

段落：以一个空行开始，以一个空行结束，中间的就是一个段落。

表格：

Item     | Value
-------- | ---
Computer | $1600
Phone    | $12
Pipe     | $1

无序列表：使用 - 加一个空格（）

- 无需列表1
- 无序列表2
- 无序列表3

有序列表：使用 数字 加一个英文句点

1\. 有序列表
2\. 有序列表
3\. 有序列表
4\. 有序列表
5\. 有序列表

换行缩进形成代码区块

    这里先换行，然后缩进4个空格，之后的内容便可以原样显示了，适合用于显示代码内容。直到文本结束或最后一个存在缩进的行为止。    

块引用
&gt;给引用的文本开始位置都加一个 '&gt;'，
&gt;便可组成一个块引用。在块引用中，可以结合
&gt;其他markdown元素一块使用，比如列表。
&gt;**强调**
也可以只在第一行加大于号，其他位置不加。

&gt;- 块引用里使用列表，需要和上面的内容隔开一个空行
&gt;- 记得加空格哦。
</code></pre>
<h2 id="如何本地安装atom插件">如何本地安装Atom插件</h2>
<p>插件安装：Settings-install，查找插件名称进行安装。但是手动安装插件速度更快，不知是不是因为墙的关系。 运行CMD</p>
<pre><code>C:\Users\alexzeng&gt;cd .atom

C:\Users\alexzeng\.atom&gt;cd packages

C:\Users\alexzeng\.atom\packages&gt;git clone https://github.com/mark-hahn/markdown-scroll-sync.git
Cloning into 'markdown-scroll-sync'...
remote: Counting objects: 177, done.
Receiving objects:  86% (153, reused 0 (delta 0), pack-reused 177
Receiving objects: 100% (177/177), 38.02 KiB | 0 bytes/s, done.
Resolving deltas: 100% (79/79), done.
Checking connectivity... done.

C:\Users\alexzeng\.atom\packages&gt;cd markdown-scroll-sync

C:\Users\alexzeng\.atom\packages\markdown-scroll-sync&gt;npm install
sub-atom@1.1.0 node_modules\sub-atom
└── jquery@2.2.4
</code></pre>
<p>手动安装成功后，需要重启Atom才能成功！</p>
<p>也可以改镜像直接安装：</p>
<blockquote>
<p>apm install atom-beautify</p>
</blockquote>
<p>如果这个安装速度太慢，还可以如下： 在terminal下运行如下命令，避开防火墙设置:</p>
<pre><code>apm config set strict-ssl false
修改registry到淘宝npm镜像

apm config set registry https://registry.npm.taobao.org
如果需要删除该镜像设置，使用：apm config delete registry
</code></pre>
<p>或者，直接用Settings</p>
<pre><code>编辑 ~/.atom/.apmrc，添加 registry = https://registry.npm.taobao.org 即可

</code></pre>
<h2 id="上传到git服务器">上传到git服务器</h2>
<p>下载Atom插件：git-control；就是命令行的GUI版本,有些类似sourcetree,但是不如它强大,日用满足</p>
<p>但是操作起来还是蛮方便的，<strong>ALT+CTRL+O</strong> 打开git-control,点击commit，然后再push 有时，会出现莫名的错误！特别是使用中文文件名。</p>
<h2 id="emmet">emmet</h2>
<p>下载emmet插件,快速html代码。</p>
<p><strong>HTML</strong></p>
<pre><code>html:5 或!：用于HTML5文档类型 —
html:xt：用于XHTML过渡文档类型 —
html:4s：用于HTML4严格文档类型 —
</code></pre>
<p><strong>id#|类.|属性[]|内容{},若是不带父元素,则默认为隐性生成(就近原则)</strong></p>
<pre><code>  &lt;!-简写格式我就放在注释里面啦啦!!--&gt;
  &lt;!--#test.test--&gt;
  &lt;div id="test" class="test"&gt;

  &lt;/div&gt;

  &lt;!-- p#test.test  --&gt;
  &lt;p id="test" class="test"&gt;&lt;/p&gt;

  &lt;!-- a[href="http://www.baidu.com"]{文本内容--我是百度} --&gt;
  &lt;a href="http://www.baidu.com"&gt;文本内容--我是百度&lt;/a&gt;
</code></pre>
<p><strong>后代&gt; | 兄弟+ | 上级^</strong></p>
<pre><code>  &lt;!-- div&gt;ul&gt;li 后代 --&gt;
  &lt;div&gt;
    &lt;ul&gt;
      &lt;li&gt;&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/div&gt;

  &lt;!-- div&gt;p+p  兄弟--&gt;
  &lt;div&gt;
    &lt;p&gt;&lt;/p&gt;
    &lt;p&gt;&lt;/p&gt;
  &lt;/div&gt;

  &lt;!-- div&gt;p&gt;ul&gt;li&gt;^span+b  上级--&gt;
  &lt;div&gt;
    &lt;p&gt;
      &lt;ul&gt;
        &lt;li&gt;&lt;/li&gt;
        &lt;span&gt;&lt;/span&gt;
        &lt;b&gt;&lt;/b&gt;
      &lt;/ul&gt;
    &lt;/p&gt;
  &lt;/div&gt;
</code></pre>
<p><em><em>分组()/乘法</em>/自增\(/自减\)@-/起序$@数字</em>*</p>
<pre><code>  &lt;!-- div&gt;ul&gt;(li&gt;a)*2 --&gt;
  &lt;div&gt;
    &lt;ul&gt;
      &lt;li&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
      &lt;li&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/div&gt;

  &lt;!-- div&gt;ul&gt;(li&gt;a{文本$$})*2 --&gt;
  &lt;!--$是匹配数字,一个代表1开始,两个01开始,依次001--&gt;
  &lt;div&gt;
    &lt;ul&gt;
      &lt;li&gt;&lt;a href=""&gt;文本01&lt;/a&gt;&lt;/li&gt;
      &lt;li&gt;&lt;a href=""&gt;文本02&lt;/a&gt;&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/div&gt;

  &lt;!-- div&gt;ul&gt;(li&gt;a{文本$@-})*3 --&gt;
  &lt;!-- @-代表启用自减,降序排列   --&gt;
  &lt;div&gt;
    &lt;ul&gt;
      &lt;li&gt;&lt;a href=""&gt;文本3&lt;/a&gt;&lt;/li&gt;
      &lt;li&gt;&lt;a href=""&gt;文本2&lt;/a&gt;&lt;/li&gt;
      &lt;li&gt;&lt;a href=""&gt;文本1&lt;/a&gt;&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/div&gt;

  &lt;!-- div&gt;ul&gt;(li&gt;a{文本$@2})*5 --&gt;
  &lt;!-- $@number 代表几号开始出现数字  --&gt;
  &lt;div&gt;
    &lt;ul&gt;
      &lt;li&gt;&lt;a href=""&gt;文本2&lt;/a&gt;&lt;/li&gt;
      &lt;li&gt;&lt;a href=""&gt;文本3&lt;/a&gt;&lt;/li&gt;
      &lt;li&gt;&lt;a href=""&gt;文本4&lt;/a&gt;&lt;/li&gt;
      &lt;li&gt;&lt;a href=""&gt;文本5&lt;/a&gt;&lt;/li&gt;
      &lt;li&gt;&lt;a href=""&gt;文本6&lt;/a&gt;&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/div&gt;
</code></pre>
<h2 id="手动修改快捷键">手动修改快捷键</h2>
<p>修改编辑器的快捷键：如果快捷发生冲突，可以在Settings-keybindings中查看是哪个插件导致错误，使用以下的语句在keymap.cson（File-keymap），使用unset!对造成冲突的快捷键停止使用。</p>
<pre><code>   'atom-text-editor:not([mini])':
     'ctrl-shift-m': 'unset!'
</code></pre>
<h2 id="代码提示，自动提醒插件">代码提示，自动提醒插件</h2>
<p>js,jquery的自动提醒插件。</p>
