# 基于协同过滤推荐算法的个性化新闻推荐系统
# Collaborative Filtering News Recommend System 
基于协同过滤算法的个性化新闻推荐系统的设计与实现（采用Java语言的SSM框架实现基于用户和物品的协同过滤推荐算法）实现了UserCF和ItemCF的协同过滤推荐算法，
Java语言（SSM框架）实现协同过滤算法的个性化新闻推荐系统，使用**基于用户和物品的协同过滤推荐算法**通过爬虫爬取环球日报新闻实现**实时计算推荐**。
**开发工具**：IDEA，jdk1.8，Mysql8，navicat数据库管理工具，Tomcat。
**后端使用**：SSM(Spring+SpringMVC+Mybatis)开发框架。
**前端使用**：javascript脚本，jquery脚本，用户端使用bootstrap前端框架，管理员端使用layui前端框架，layer弹窗组件等。
# 功能实现
**系统前台**：用户具有注册、登录、注销、浏览新闻、搜索新闻、信息修改、密码修改、喜好标签、新闻评分、新闻收藏、新闻评论、排行榜、热点推荐、个性化推荐新闻等功能；
**后台管理系统**：管理员可以查看数据统计、用户管理、新闻管理、新闻类型管理、评分管理、收藏管理、评论管理、浏览记录管理、用户喜好标签等。
**协同过滤推荐功能**：
 1. **热点榜单**
	 根据数据库的新闻数据查询浏览数量最多的新闻进行推荐，同时查询出来的是不包括当前登录用户已经浏览过的新闻（过滤当前用户已经浏览过的新闻）；
 2. **个性化推荐**
    2.1. 游客：根据新闻总评分和总收藏数量降序查询输出向游客推荐。
    2.2. 登录用户：
    **基于用户的协同过滤推荐算法**：根据新闻的评分数据采用基于用户的协同过滤推荐算法实时计算向用户进行新闻推荐；如果没有推荐结果，采用根据登录用户选择的喜好标签下的新闻的总评分降序推荐，同时推荐的新闻是过滤掉当前登录用户已经评分过的新闻；
   **基于项目的协同过滤推荐算法**：根据新闻的收藏数量采用基于项目的协同过滤推荐算法从高到低降序向用户进行推荐；如果没有推荐结果，采用根据登录用户喜好标签下的新闻的收藏数量降序推荐，同时推荐的是当前登录用户没有收藏过的新闻。
 3. **相关推荐**
     推荐当前登录用户正在浏览的新闻相同类型下评分较高的新闻，同时推荐的是当前用户没有评分的新闻。
**新闻数据来源**：爬取环球日报新闻数据
**源码获取**： +v：18484646674   +QQ:2474345497
**项目临时演示地址**：项目在线演示地址
**前台**：http://113.125.137.7:26/NewsRecommendOnline/
**后台**：http://113.125.137.7:26/NewsRecommendOnline/admin/login
**项目结构**
![项目结构](https://img-blog.csdnimg.cn/direct/76890d003dd74430930e6835e44752a9.png#pic_center)
![数据库](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/e4dfeab7-f776-4e1e-a126-957baca47914)
![数据库](https://gitee.com/ss-i-gg/CollaborativeFilteringNewsRecommendSystem/raw/main/%E5%8D%8F%E5%90%8C%E8%BF%87%E6%BB%A4%E6%8E%A8%E8%8D%90.jpg)
**前台系统**
![Inked首页](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/8dfa903f-3a78-4a85-854c-f6d2ce6c6be5)
![Inked新闻查看](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/70bcd0e7-844c-49fd-89db-a2f448f56e64)
![登录](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/cfce9455-8ac7-40fa-b0c6-906ccc5e8c49)
![登录选择喜好标签](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/3ac79cf4-fcdb-47dc-90bd-4fb2bb17d2d0)
![Inked个人中心](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/eae37196-e3f7-4526-80db-56c951a7a449)
![Inked个人中心密码修改](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/c82926f8-b0ef-46f1-a405-1e5975d5772f)
![Inked我的收藏](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/350c5de8-920d-41ff-920c-381c155fd50a)
![兴趣标签](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/eda8c24e-5c5f-4e14-b6d3-adc854dff36b)
**后台管理系统**
![后台登录](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/d8e10202-902f-4f06-bc7b-ecc7b8cf033d)
![后台首页](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/cda419f1-17c6-411b-8a61-0c1ae9ab2246)
![Inked新闻管理](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/22526ea5-4cf9-4ef3-9cb9-2d49165462ea)
![Inked用户管理](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/06fa51b6-3db7-461d-8fbd-c5ff0ad2fd42)
![Inked管理员管理](https://github.com/songwo-153/NewsRecommendOnline/assets/86769062/ab09605d-5a8f-4978-a9d7-959bdf8147e8)
**源码获取**：[基于协同过滤算法新闻推荐系统源码.zip](https://github.com/songwo-153/CollaborativeFilteringNewsRecommendSystem/files/13557079/default.zip)



