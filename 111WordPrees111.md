# WordPrees新闻站流程
## 一、域名+服务器
### 1. 查看域名属性、含义，使用IA生成标题、简介、ico图片（记得翻译看看）
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/af7a1d0d-fd34-4424-a798-2831b7173005)
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/5d5d4d08-19d9-4f47-a6b5-dd2c77588081)

### 2. 按照域名含义创建分类目录。（如没有含义，则自己定义）
    例如：
            历史 History
            财经 Finance
            商业 Business
            娱乐 Entertainment
            旅游 Travel
            政治 Political

### 3. 解析域名到对应服务器，登录服务器配置网站，上传wordpress程序包，登录wordpress后台
## 二、WordPress后台设置
### 1. 创建分类目录（一般3个左右）
        文章
            分类目录
                名称（分类目录名称）
                别名（url格式，大写换小写） 
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/636a5aeb-6844-43cd-8e83-cd3a066eb634)


### 2. 主题
        外观
            主题（选择试用的主题，换着用）
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/0c4bd293-20d0-44b9-bd31-041e1149fd85)

            自定义（设置ico图片）
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/1b6edfd9-dba6-482c-ad0b-5547eee89500)

![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/7ee139db-5552-44c3-9d16-c561aaa98176)

            菜单（添加分类目录到网站显示，记得排序）
                查看所有
                    分类目录
                        查看所有（勾选你创建的分类，添加到菜单）
                            菜单设置
                                勾选 自动将新的顶级页面添加至菜单
                                勾选 Main Menu
                                        保存保存保存
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/758883bb-3e7f-4345-81f2-49c1ade0a156)



### 3. 插件
        上传插件，并查看上传的插件是否启动，没有的话。手动点击启动
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/e7ee351c-72f0-4e6e-ad3e-d3688fd39380)

    
        
### 4. 工具
        禁用评论
            勾选 任何地方 在整个网站上全局禁用评论（保存）
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/971b5497-d3c3-415b-8e79-07872007575c)

        Head & Footer Code (添加yandex统计)
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/4cefa7ae-b615-47f6-a249-fe0d65fbfb57)
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/834c8905-ed8c-47e1-8594-969e2652b059)

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

### 5. 设置
        常规（配置网站标题）
![image](https://github.com/cow-study-notes/Wordpress/assets/105910804/5bd826c0-ec16-416d-a63c-aaf82f28e8b4)

        关闭底部Privacy Policy-隐私政策分类目录
![image](https://github.com/cow-study-notes/Wordpress/assets/105910804/0cf95750-da94-4303-bf1c-3b02beeb3bef)

### 6.Yoast SEO
            设置
                内容类型
                        首页
                            添加网站描述          
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/9231da3f-8233-4217-8d2f-9c23dde40557)

            工具
                启动开始收集SEO数据
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/c39012f6-1a0e-4330-8424-a1b0a0458c3d)

### 7.Automatic
        New campaign (这里先一个一个创建你的分类，创建完成，我们去改数据库，直接导入预设好的配置)     
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/9027d2d2-4022-477a-b897-cf50d4483b2e)
### 数据库主要改
                    camp_post_title
                            [original_title]
                    camp_post_content
                            [matched_content]
                    camp_options
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/10fc7641-9cf3-4f71-b515-3a083459d126)
a:45:{i:0;s:11:"OPT_STRIP_T";i:1;s:16:"OPT_MUST_CONTENT";i:2;s:20:"OPT_FEED_CONVERT_ENC";i:3;s:17:"OPT_FEED_ENCODING";i:4;s:15:"OPT_FEED_SCRIPT";i:5;s:30:"OPT_FEED_LAZY_NOSCRIPT_DISABLE";i:6;s:12:"OPT_CJ_CACHE";i:7;s:12:"OPT_AE_CACHE";i:8;s:12:"OPT_CL_CACHE";i:9;s:12:"OPT_WM_CACHE";i:10;s:12:"OPT_PL_CACHE";i:11;s:12:"OPT_RD_CACHE";i:12;s:21:"OPT_RD_OFFICIAL_EMBED";i:13;s:12:"OPT_IU_CACHE";i:14;s:12:"OPT_EV_CACHE";i:15;s:21:"OPT_GENERATE_FB_TITLE";i:16;s:12:"OPT_FB_CACHE";i:17;s:14:"OPT_AM_GALLERY";i:18;s:12:"OPT_VM_CACHE";i:19;s:16:"OPT_GP_REMOVE_H1";i:20;s:12:"OPT_SC_CACHE";i:21;s:12:"OPT_PT_CACHE";i:22;s:17:"OPT_PT_AUTO_TITLE";i:23;s:12:"OPT_IT_CACHE";i:24;s:17:"OPT_IT_AUTO_TITLE";i:25;s:16:"OPT_TW_VID_EMBED";i:26;s:9:"OPT_TW_RT";i:27;s:9:"OPT_TW_RE";i:28;s:12:"OPT_DM_CACHE";i:29;s:12:"OPT_YT_CACHE";i:30;s:12:"OPT_EB_CACHE";i:31;s:12:"OPT_FL_CACHE";i:32;s:18:"OPT_CB_DESCRIPTION";i:33;s:18:"OPT_OPENAI_PENDING";i:34;s:9:"OPT_THUMB";i:35;s:14:"OPT_THUMB_ALT2";i:36;s:14:"OPT_THUMB_ALT3";i:37;s:16:"OPT_FEEDS_OG_IMG";i:38;s:9:"OPT_CACHE";i:39;s:15:"OPT_CACHE_CLEAN";i:40;s:7:"OPT_TBS";i:41;s:11:"OPT_TBS_TTL";i:42;s:9:"OPT_STRIP";i:43;s:16:"OPT_STRIP_INLINE";i:44;s:13:"OPT_LINK_ONCE";}

### 删除HTML标记 (找不到就搜索：删除HTML标记)
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/e82b39b6-8eba-480a-914e-1151bf809ba9)
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/d1f9544d-a03e-4e49-9584-79453edd95a9)

### 选择你文章要发到的对应分类目录 (找不到就搜索：Post posts to this category)
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/f649e314-3552-413b-80a8-6801a12838b6)

### 搜索你需要的Feed源（http://107.148.47.10:5000/）
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/9041bcf9-6b89-40e6-a984-6c690ecc9c20)

### 添加Feed源测试文章是否正常
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/dae075b5-7508-450b-bb94-bb7350c8fe19)

### Feed的测试文章记得删除
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/1262cd56-9922-4cdc-8afb-a255dd0fa1a4)

### 清除一下页面缓存 (找不到就搜索：Actions)
![image](https://github.com/cow-study-notes/Wordpress-/assets/105910804/4abc0ae8-f817-4d64-8677-09f3a245583d)

##### 设置完了（访问网站检测有没有遗漏，再看看Wordpress配置有没有遗漏）
#### 设置完了（访问网站检测有没有遗漏，再看看Wordpress配置有没有遗漏）
### 设置完了（访问网站检测有没有遗漏，再看看Wordpress配置有没有遗漏）
## 设置完了（访问网站检测有没有遗漏，再看看Wordpress配置有没有遗漏）
# 设置完了（访问网站检测有没有遗漏，再看看Wordpress配置有没有遗漏）
