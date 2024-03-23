# 计算机科学与编程入门课程第一次作业
## 2000018601 陈佳琪

## 1. 作业1
为了解中国2022年各省市地区的就业人员数，从[中国统计年鉴网站](https://www.stats.gov.cn/sj/ndsj/2023/indexch.htm)收集了分地区就业人员数，利用pycharts的geo模块生成了中国各地区就业人员情况图（不含港澳台）。

该图可以将各地区的就业人员数对应到地理坐标上，直观清晰地呈现了各地区就业人员在数量上的差异，并依据就业数将各省份分为5个梯队：0-1400万人；1400-2800万人；2800-4200万人；4200-5600万人；5600-7000万人，图例支持梯队筛选功能。

每个梯队的省份用不同颜色的散点标注，散点鼠标悬停可以看见对应的省份名称和就业人数。


为了解YouTube视频网站在全球的用户规模，从[DATAREPORTAL](https://datareportal.com/)收集了2024年油管用户规模TOP20的国家，利用pycharts的map模块将结果可视化。

该图可以将各国的油管用户数对应到世界地图上，鼠标悬停即显示国家名称和对应用户数；根据用户数可将国家分为5个梯队，颜色越深色调越暖代表用户规模越大。可以直观明了地观察到油管用户在全世界各国的分布。

[作业1链接]
(https://joychen28.github.io/geo-2022China_employment.html)
(https://joychen28.github.io/Map-2024YouTube_user_top20.html)

## 2. 作业2
随着互联网的普及和发展，世界各国的上网率在不断升高，为了解阿拉伯国家的互联网普及率和网民情况，从[DATAREPORTAL](https://datareportal.com/)收集了2022年阿拉伯国家的互联网用户数、普及率、社交媒体活跃用户数、Facebook渗透率，以及普及率最高的沙特和阿联酋两国的人口结构，最后利用pycharts的组合图表功能将结果可视化。

图1（line）以折线图形式呈现了阿拉伯国家的互联网普及率和Facebook渗透率，并标记了极值点，折线图的形式可以很好反映出各国的互联网普及程度，阿联酋和沙特是互联网普及率最高的两个阿拉伯国家；同时，可以看出Facebook的用户规模在各个国家中存在很大差异，其中阿联酋和利比亚是Facebook用户基础最广泛的两个国家，但无法看出互联网普及率和Facebook渗透率存在相关性。

为了进一步观察互联网普及和社交媒体平台发展之间的关系，我收集了各国的网民数和社交媒体活跃用户数，并生成bar柱状图（图3 grid），通过对比可以得出互联网用户数和社交媒体活跃用户数存在正相关关系，沙特和埃及是网民规模最大的两个阿拉伯国家。图中还叠加了Facebook渗透率的折线图，单选“社交媒体活跃数”发现，总体上Facebook渗透率指标和社交媒体活跃用户数呈正相关。

为进一步观察阿拉伯国家网民情况，我选取沙特和阿联酋这两个互联网普及率最高的国家进行进一步观察，收集了2022年两国的人口结构分布，并用图2（玫瑰图）结果可视化。

玫瑰图不仅美观，而且还能清晰呈现出人口年龄的结构性分布。从图中可以看出，沙特和阿联酋的人口主要集中在Y世代（25-44岁），人口比例最小的都是“婴儿潮”时代（55-65岁），但阿联酋人口老龄化程度更高，因为X世代（45-54岁）的占比更高。由此可以合理猜测，沙特和阿联酋的主要网民年龄位于25-44岁，都是中青年群体。

[作业2链接](https://joychen28.github.io/tab-2022arabic_internet_user.html)

## 3. 作业3
近几年人工智能飞速发展，美国和中国是投资人工智能技术规模最大的两个国家，但在阿拉伯地区，人工智能的发展也在兴起，尤其是资金雄厚的海湾国家，以沙特和阿联酋为代表，正如火如荼进行”世界第四次经济革命”。

为了解阿拉伯社会对人工智能的看法和关注话题，我利用网络爬虫技术（ParseHub）爬取了沙特国有国际新闻频道Al Arabiya网站的相关报道，以“االذكاء الاصطناعي”（人工智能）为检索词共爬取报道2600+篇，包括标题、时间、地点和新闻文本，以段落为单位共收集2.7w+文本数，时间从2013年2月到2024年3月。

图1（worldcloud）生成了2.7w篇幅中词频前100的单词。
在统计词频时，首先加载阿拉伯语停用词词表（github），并手动加入阿拉伯语特殊符号进行文本预处理，在此基础上对文本进行分词并遍历统计。

图2（timeline）在图1的基础上进行了报道年份的分组，并加上时间线统计了2013-2024各个年份新闻报道中的前十高频词，以柱状图呈现，且有多个横轴标签，由此可以观察出各年份对人工智能关注领域的异同。

图3（News Count by Year）以柱状图呈现了各年份新闻报道的篇幅数变化。利用count函数计算各年份的出现次数，从而生成不同年份新闻报道篇幅的柱状图。由此可以看出人工智能热度的时间变化趋势。

图4（News Count by Location）以bar+timeline的形式呈现了不同国家和地区报道人工智能相关新闻的篇幅，同样是利用counts函数对地点进行统计，但不涉及分词和停用词过滤。由此可以清晰看出各个国家和地区对人工智能的关注度。

[作业3链接](https://joychen28.github.io/ALARABIYA_AI_News.html)
