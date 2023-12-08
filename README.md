# xhs
小红书api接口,小红书数据采集

-----------------------------------------------------------------小红书WEB端api数据接口-----------------------------------------------------------
一、主题列表：
http://helpnow.top:8083/topics?key=xxxxxx&page_id=5d09a3fe1b1dc9000136db47&sort=hot&cursor=
page_id为话题分享页的id，如 5d09a3fe1b1dc9000136db47
cursor为翻页参数，从前一页返回里可获取下一页所需的cursor参数，首页传空
sort：排序，可取之为hot与time，默认为hot，表示按热度排序，time表示按最新排序

二、用户详情页作品列表：
http://helpnow.top:8083/user/notes?key=xxxxxx&user_id=55d99833f5a26377a030cbf8&cursor=


三、笔记详情页：
http://helpnow.top:8083/feed?key=xxxxxx&note_id=5b275e5c9374260197ec884a

四、搜索列表：
http://helpnow.top:8083/search?key=xxxxxx&keyword=变形金刚&page=1
第二页（加参数）：
http://helpnow.top:8083/search?key=xxxxxx&keyword=变形金&page=1&note_type=1&sort=popularity_descending
keyword:搜索关键字（必须）
page:页号（必须）从第一页开始
note_type：搜索筛选(默认0综合):0:综合；1：视频筛选；2：图文筛选；
sort:搜索排序（默认general综合排序）；sort=popularity_descending最热；sot=time_descending最新；

五、笔记评论：
http://helpnow.top:8083/comment?key=xxxxxx&note_id=63e77ef7000000001300a9e3&cursor=
cursor为翻页参数，从前一页返回里可获取下一页所需的cursor参数，首页传空

六、评论回复：
http://helpnow.top:8083/comment?key=xxxxxx&note_id=63e77ef7000000001300a9e3&root_comment_id=640b7dad000000000700ded2&cursor=
cursor为翻页参数，从前一页返回里可获取下一页所需的cursor参数，首页传空

七、用户基本信息：
http://helpnow.top:8083/user/info?key=xxxxxx&user_id=5aa12b5311be107df912efb4

八、无水印feed
http://helpnow.top:8083/explore?key=xxxxxx&note_id=65323f4c000000002402ddfc
http://helpnow.top:8083/explore?key=xxxxxx&note_id=65323f4c000000002402ddfc&parse=true

九、主页推荐列表
http://helpnow.top:8083/homefeed?key=xxxxxx&category=homefeed_recommend&note_index=26&cursor_score=1.694573379973002E9



-----------------------------------------------------------------小红书APP端api接口-----------------------------------------------------------
-----------------------------------------------------------------首页笔记推荐列表-----------------------------------------------------------
默认：推荐
http://helpnow.top:8083/wx/homefeed?key=xxxxxx&page=1
推荐
http://helpnow.top:8083/wx/homefeed?key=xxxxxx&category=homefeed_recommend&page=1
时尚
http://helpnow.top:8083/wx/homefeed?key=xxxxxx&category=homefeed_fashion&page=1
{"code":0,"success":true,"data":[{"name":"推荐","oid":"recommend_v2"},{"name":"时尚","oid":"homefeed.fashion_v2"},{"name":"护肤","oid":"homefeed.skincare_v2"},{"name":"彩妆","oid":"homefeed.cosmetics_v2"},{"name":"美食","oid":"homefeed.food_v2"},{"name":"旅行","oid":"homefeed.travel_v2"},{"name":"影视","oid":"homefeed.movies_v2"},{"name":"读书","oid":"homefeed.books_v2"},{"name":"明星","oid":"homefeed.celebrities_v2"},{"name":"健身","oid":"homefeed.fitness_v2"},{"name":"家居","oid":"homefeed.home_v2"},{"name":"宠物","oid":"homefeed.pets_v2"},{"name":"音乐","oid":"homefeed.music_v2"},{"name":"婚礼","oid":"homefeed.weddings_v2"},{"name":"母婴","oid":"homefeed.maternity_v2"},{"name":"萌娃","oid":"homefeed.baby_v2"},{"name":"数码","oid":"homefeed.digital_v2"},{"name":"汽车","oid":"homefeed.car_v2"},{"name":"男士穿搭","oid":"homefeed.mens_fashion_v2"}]}


-----------------------------------------------------------------用户中心-----------------------------------------------------------
用户信息（个人页）
http://helpnow.top:8083/wx/user/info?key=xxxxxx&user_id=5aa12b5311be107df912efb4

http://helpnow.top:8083/wx/user/info?key=xxxxxx&user_id=59a8bc095e87e774ad40f346
https://www.xiaohongshu.com/user/profile/59a8bc095e87e774ad40f346
收藏
http://helpnow.top:8083/wx/user/collectedNotes?key=xxxxxx&user_id=59a8bc095e87e774ad40f346
wx 登录用户信息（个人资料页）
http://helpnow.top:8083/wx/user/me?key=xxxxxx
-wx 用户发表的作品列表（个人页）
http://helpnow.top:8083/wx/user/notes?key=xxxxxx&user_id=59a8bc095e87e774ad40f346

-----------------------------------------------------------------笔详页-----------------------------------------------------------
笔记详情
http://helpnow.top:8083/wx/feed?key=xxxxxx&note_id=5b275e5c9374260197ec884a

1、评论第一页：
http://helpnow.top:8083/wx/comment?key=xxxxxx&note_id=63e77ef7000000001300a9e3
2、评论第二页：
end_id为上一页的最后一个评论的id。
http://helpnow.top:8083/wx/comment?key=xxxxxx&note_id=63e77ef7000000001300a9e3&end_id=63f6ffe50000000017012064
-----------------------------------------------------------------笔记搜索-----------------------------------------------------------
关键词app搜索接口：
http://helpnow.top:8083/wx/search?key=xxxxxx&keyword=变形金刚&page=1&sort=general
sort=general综合排序；sort=hot_desc按热度排序；sort=create_time_desc按时间排序；默认：综合排序




其中，key=xxxxxx为访问令牌，联系：QQ：39848872，微信：byc6352，telegram:byc01，可以拿到令牌。另外有，京东，淘宝，抖音等各类api数据接口也有。
