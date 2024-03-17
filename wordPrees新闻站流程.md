# WordPrees新闻站流程
### 一、域名+服务器
    1.查看域名属性、含义，使用IA生成标题、简介、ico图片（记得翻译看看）

    2.按照域名含义创建分类目录。（如没有含义，则自己定义）
        例如：
                历史 History
                财经 Finance
                商业 Business
                娱乐 Entertainment
                旅游 Travel
                政治 Political

    3.解析域名到对应服务器，登录服务器配置网站，上传wordpress程序包，登录wordpress后台
### 二、WordPress后台设置
    1.创建分类目录（一般3个左右）
        文章
            分类目录
                名称（分类目录名称）
                别名（url格式，大写换小写） 


    2.主题
        外观
            主题（选择试用的主题，换着用）
            自定义（设置ico图片）
            菜单（添加分类目录到网站显示，记得排序）
                查看所有
                    分类目录
                        查看所有（勾选你创建的分类，添加到菜单）
                            菜单设置
                                勾选 自动将新的顶级页面添加至菜单
                                勾选 Main Menu
                                        保存保存保存


    3.插件
        上传插件，并查看上传的插件是否启动，没有的话。手动点击启动


    
        
    4.工具
        禁用评论
            勾选 任何地方 在整个网站上全局禁用评论（保存）

        Head & Footer Code (添加yandex统计)
```html
<!-- Yandex.Metrika counter -->
<script type="text/javascript" >
   (function(m,e,t,r,i,k,a){m[i]=m[i]function(){(m[i].a=m[i].a[]).push(arguments)};
   m[i].l=1*new Date();
   for (var j = 0; j < document.scripts.length; j++) {if (document.scripts[j].src === r) { return; }}
   k=e.createElement(t),a=e.getElementsByTagName(t)[0],k.async=1,k.src=r,a.parentNode.insertBefore(k,a)})
   (window, document, "script", "https://mc.yandex.ru/metrika/tag.js", "ym");

   ym(96746980, "init", {
        clickmap:true,
        trackLinks:true,
        accurateTrackBounce:true,
        webvisor:true
   });
</script>
<noscript><div><img src="https://mc.yandex.ru/watch/96746980" style="position:absolute; left:-9999px;" alt="" /></div></noscript>
<!-- /Yandex.Metrika counter -->
```

    5.Yoast SEO
            设置
                内容类型
                    首页
                        添加
            工具
                启动开始收集SEO数据
