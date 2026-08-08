# Cursor开源MoK框架提速MoE训练41%

**2026年7月17日 12时34分56秒**

---

Cursor团队开源MoK底层优化框架，通过重排GPU流水线、重叠通信与专家路由缓存，使MoE训练吞吐提升41%。MoE是大模型降本主流结构，但专家并行带来all-to-all通信瓶颈，MoK把Token分发时机与NVLink拓扑对齐，特别适合长上下文。开源后中小团队用更少卡跑通千亿MoE，削弱头部厂算力护城河。也呼应PyTorch、Megatron生态“软硬协同”回归——同样H100，调度算法能吃掉近半代际差。对国产卡异构集群，MoK思路可改写通信后端适配。

---

[App Usage](https://www.xiazainiao.com/xiazai/74594.html) | [二建市政工程视频app](https://www.xiazainiao.com/xiazai/74595.html) | [水相游戏](https://www.xiazainiao.com/xiazai/74596.html) | [陕西气象app](https://www.xiazainiao.com/xiazai/74597.html) | [指尖像素城官方版](https://www.xiazainiao.com/xiazai/74598.html) | [欢乐水杯](https://www.xiazainiao.com/xiazai/74599.html) | [以闪亮之名国际服](https://www.xiazainiao.com/xiazai/74600.html) | [修图去水印app](https://www.xiazainiao.com/xiazai/74601.html) | [云游宝](https://www.xiazainiao.com/xiazai/74602.html) | [胜芳大杂烩app](https://www.xiazainiao.com/xiazai/74603.html)

来源依据：
来源依据：[华为MateBookPro获AI终端L3级国标首证.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%8D%8E%E4%B8%BAMateBookPro%E8%8E%B7AI%E7%BB%88%E7%AB%AFL3%E7%BA%A7%E5%9B%BD%E6%A0%87%E9%A6%96%E8%AF%81.md)<br>
[中国科学家在量子计算纠错领域取得重大突破.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%AD%E5%9B%BD%E7%A7%91%E5%AD%A6%E5%AE%B6%E5%9C%A8%E9%87%8F%E5%AD%90%E8%AE%A1%E7%AE%97%E7%BA%A0%E9%94%99%E9%A2%86%E5%9F%9F%E5%8F%96%E5%BE%97%E9%87%8D%E5%A4%A7%E7%AA%81%E7%A0%B4.md)<br>
[SK海力士与SanDisk发布HBF规范.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/SK%E6%B5%B7%E5%8A%9B%E5%A3%AB%E4%B8%8ESanDisk%E5%8F%91%E5%B8%83HBF%E8%A7%84%E8%8C%83.md)<br>
[AI驱动的药物晶型预测加速仿制药上市.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/AI%E9%A9%B1%E5%8A%A8%E7%9A%84%E8%8D%AF%E7%89%A9%E6%99%B6%E5%9E%8B%E9%A2%84%E6%B5%8B%E5%8A%A0%E9%80%9F%E4%BB%BF%E5%88%B6%E8%8D%AF%E4%B8%8A%E5%B8%82.md)<br>
[2026年暑期档电影票房突破55亿元.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/2026%E5%B9%B4%E6%9A%91%E6%9C%9F%E6%A1%A3%E7%94%B5%E5%BD%B1%E7%A5%A8%E6%88%BF%E7%AA%81%E7%A0%B455%E4%BA%BF%E5%85%83.md)<br>
[新能源船舶补给标准统一实施.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%96%B0%E8%83%BD%E6%BA%90%E8%88%B9%E8%88%B6%E8%A1%A5%E7%BB%99%E6%A0%87%E5%87%86%E7%BB%9F%E4%B8%80%E5%AE%9E%E6%96%BD.md)<br>
[携程公布19项整改措施回应监管.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%90%BA%E7%A8%8B%E5%85%AC%E5%B8%8319%E9%A1%B9%E6%95%B4%E6%94%B9%E6%8E%AA%E6%96%BD%E5%9B%9E%E5%BA%94%E7%9B%91%E7%AE%A1.md)<br>
[600多根三星堆古象牙搬入新家.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/600%E5%A4%9A%E6%A0%B9%E4%B8%89%E6%98%9F%E5%A0%86%E5%8F%A4%E8%B1%A1%E7%89%99%E6%90%AC%E5%85%A5%E6%96%B0%E5%AE%B6.md)<br>
[小荷健康发布MedXIAOHE疑难病例诊疗评测基准1.0.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%B0%8F%E8%8D%B7%E5%81%A5%E5%BA%B7%E5%8F%91%E5%B8%83MedXIAOHE%E7%96%91%E9%9A%BE%E7%97%85%E4%BE%8B%E8%AF%8A%E7%96%97%E8%AF%84%E6%B5%8B%E5%9F%BA%E5%87%861.0.md)<br>
[国内首个量子精密测量产业化基地在合肥启用.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%9B%BD%E5%86%85%E9%A6%96%E4%B8%AA%E9%87%8F%E5%AD%90%E7%B2%BE%E5%AF%86%E6%B5%8B%E9%87%8F%E4%BA%A7%E4%B8%9A%E5%8C%96%E5%9F%BA%E5%9C%B0%E5%9C%A8%E5%90%88%E8%82%A5%E5%90%AF%E7%94%A8.md)<br>

[银河战士融合](https://www.xiazainiao.com/xiazai/74604.html) | [爱设计app](https://www.xiazainiao.com/xiazai/74605.html) | [催化剂加app](https://www.xiazainiao.com/xiazai/74606.html) | [apabi reader阅读器手机版](https://www.xiazainiao.com/xiazai/74607.html) | [芒果修图官方版](https://www.xiazainiao.com/xiazai/74608.html) | [康爱多掌上药店](https://www.xiazainiao.com/xiazai/74609.html) | [康爱多网上药店安卓版](https://www.xiazainiao.com/xiazai/74610.html) | [爱音斯坦fm官方版](https://www.xiazainiao.com/xiazai/74611.html) | [得言app](https://www.xiazainiao.com/xiazai/74612.html) | [考护狮官方版](https://www.xiazainiao.com/xiazai/74613.html)

来源依据：
来源依据：[全球首款AI智能体手机NaviXUltra发布.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%85%A8%E7%90%83%E9%A6%96%E6%AC%BEAI%E6%99%BA%E8%83%BD%E4%BD%93%E6%89%8B%E6%9C%BANaviXUltra%E5%8F%91%E5%B8%83.md)<br>
[zt_060_md_hybrid_20260617.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/zt_060_md_hybrid_20260617.md)<br>
[植物基鸡蛋替代品烘焙性能媲美真蛋.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%A4%8D%E7%89%A9%E5%9F%BA%E9%B8%A1%E8%9B%8B%E6%9B%BF%E4%BB%A3%E5%93%81%E7%83%98%E7%84%99%E6%80%A7%E8%83%BD%E5%AA%B2%E7%BE%8E%E7%9C%9F%E8%9B%8B.md)<br>
[SK与英伟达锁HBM长协.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/SK%E4%B8%8E%E8%8B%B1%E4%BC%9F%E8%BE%BE%E9%94%81HBM%E9%95%BF%E5%8D%8F.md)<br>
[中小学生劳动教育评价体系健全.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%AD%E5%B0%8F%E5%AD%A6%E7%94%9F%E5%8A%B3%E5%8A%A8%E6%95%99%E8%82%B2%E8%AF%84%E4%BB%B7%E4%BD%93%E7%B3%BB%E5%81%A5%E5%85%A8.md)<br>
[zt_030_resource_detailed_20260617.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/zt_030_resource_detailed_20260617.md)<br>
[zt_011_headline_ts_batch2_20260613.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/zt_011_headline_ts_batch2_20260613.md)<br>
[“中国天眼”揭示低能宇宙线起源新证据.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E2%80%9C%E4%B8%AD%E5%9B%BD%E5%A4%A9%E7%9C%BC%E2%80%9D%E6%8F%AD%E7%A4%BA%E4%BD%8E%E8%83%BD%E5%AE%87%E5%AE%99%E7%BA%BF%E8%B5%B7%E6%BA%90%E6%96%B0%E8%AF%81%E6%8D%AE.md)<br>
[zt_023_headline_group_20260617.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/zt_023_headline_group_20260617.md)<br>
[景德镇手工瓷业遗存申遗.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%99%AF%E5%BE%B7%E9%95%87%E6%89%8B%E5%B7%A5%E7%93%B7%E4%B8%9A%E9%81%97%E5%AD%98%E7%94%B3%E9%81%97.md)<br>

[牧场物语记忆的种子汉化破解版](https://www.xiazainiao.com/xiazai/74614.html) | [苏州线上教育中心平台app](https://www.xiazainiao.com/xiazai/74615.html) | [苏州线上教育app](https://www.xiazainiao.com/xiazai/74616.html) | [苏州线上教育学生版](https://www.xiazainiao.com/xiazai/74617.html) | [苏州线上教育在线版](https://www.xiazainiao.com/xiazai/74618.html) | [武林的传说手游](https://www.xiazainiao.com/xiazai/74619.html) | [12326民航官方app](https://www.xiazainiao.com/xiazai/74620.html) | [身份小卫士app](https://www.xiazainiao.com/xiazai/74621.html) | [公交出行app\(原帮帮公交\)](https://www.xiazainiao.com/xiazai/74622.html) | [专技天下app](https://www.xiazainiao.com/xiazai/74623.html)

来源依据：
来源依据：[zt_009_headline_bar_20260612.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/zt_009_headline_bar_20260612.md)<br>
[rj_040_md_hybrid_20260617.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/rj_040_md_hybrid_20260617.md)<br>
[国内首个商业化地热能直接利用项目在雄安投运.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%9B%BD%E5%86%85%E9%A6%96%E4%B8%AA%E5%95%86%E4%B8%9A%E5%8C%96%E5%9C%B0%E7%83%AD%E8%83%BD%E7%9B%B4%E6%8E%A5%E5%88%A9%E7%94%A8%E9%A1%B9%E7%9B%AE%E5%9C%A8%E9%9B%84%E5%AE%89%E6%8A%95%E8%BF%90.md)<br>
[中国羽毛球公开赛刘圣书谭宁卫冕.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%AD%E5%9B%BD%E7%BE%BD%E6%AF%9B%E7%90%83%E5%85%AC%E5%BC%80%E8%B5%9B%E5%88%98%E5%9C%A3%E4%B9%A6%E8%B0%AD%E5%AE%81%E5%8D%AB%E5%86%95.md)<br>
[三一纯电重卡跑出赛道单圈纪录.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%89%E4%B8%80%E7%BA%AF%E7%94%B5%E9%87%8D%E5%8D%A1%E8%B7%91%E5%87%BA%E8%B5%9B%E9%81%93%E5%8D%95%E5%9C%88%E7%BA%AA%E5%BD%95.md)<br>
[中国首次跻身全球创新指数排名前十.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%AD%E5%9B%BD%E9%A6%96%E6%AC%A1%E8%B7%BB%E8%BA%AB%E5%85%A8%E7%90%83%E5%88%9B%E6%96%B0%E6%8C%87%E6%95%B0%E6%8E%92%E5%90%8D%E5%89%8D%E5%8D%81.md)<br>
[上海发布全国首部法律服务大模型部署指引.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%8A%E6%B5%B7%E5%8F%91%E5%B8%83%E5%85%A8%E5%9B%BD%E9%A6%96%E9%83%A8%E6%B3%95%E5%BE%8B%E6%9C%8D%E5%8A%A1%E5%A4%A7%E6%A8%A1%E5%9E%8B%E9%83%A8%E7%BD%B2%E6%8C%87%E5%BC%95.md)<br>
[上海发布星枢计划首发太空算力星座.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%8A%E6%B5%B7%E5%8F%91%E5%B8%83%E6%98%9F%E6%9E%A2%E8%AE%A1%E5%88%92%E9%A6%96%E5%8F%91%E5%A4%AA%E7%A9%BA%E7%AE%97%E5%8A%9B%E6%98%9F%E5%BA%A7.md)<br>
[人工智能优化残疾人就业匹配.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%BA%BA%E5%B7%A5%E6%99%BA%E8%83%BD%E4%BC%98%E5%8C%96%E6%AE%8B%E7%96%BE%E4%BA%BA%E5%B0%B1%E4%B8%9A%E5%8C%B9%E9%85%8D.md)<br>
[SpaceX重心转向月球计划建自生长月城.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/SpaceX%E9%87%8D%E5%BF%83%E8%BD%AC%E5%90%91%E6%9C%88%E7%90%83%E8%AE%A1%E5%88%92%E5%BB%BA%E8%87%AA%E7%94%9F%E9%95%BF%E6%9C%88%E5%9F%8E.md)<br>

[专技天下继续教育网app](https://www.xiazainiao.com/xiazai/74624.html) | [威力省电神器\(power battery\)](https://www.xiazainiao.com/xiazai/74625.html) | [剪影多多软件](https://www.xiazainiao.com/xiazai/74626.html) | [剑与魔宠官方版](https://www.xiazainiao.com/xiazai/74627.html) | [钢笔书法官方版](https://www.xiazainiao.com/xiazai/74628.html) | [下坠灌篮纯净版](https://www.xiazainiao.com/xiazai/74629.html) | [07072手游盒子app](https://www.xiazainiao.com/xiazai/74630.html) | [猴面包树游戏](https://www.xiazainiao.com/xiazai/74631.html) | [冒险岛M手游官方正版](https://www.xiazainiao.com/xiazai/74632.html) | [美酒点评app](https://www.xiazainiao.com/xiazai/74633.html)

来源依据：
来源依据：[rj_039_md_hybrid_20260617.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/rj_039_md_hybrid_20260617.md)<br>
[国际射联全项世界杯杭州站破纪录.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%9B%BD%E9%99%85%E5%B0%84%E8%81%94%E5%85%A8%E9%A1%B9%E4%B8%96%E7%95%8C%E6%9D%AF%E6%9D%AD%E5%B7%9E%E7%AB%99%E7%A0%B4%E7%BA%AA%E5%BD%95.md)<br>
[小荷健康发布MedXIAOHE医疗评测基准1.0.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%B0%8F%E8%8D%B7%E5%81%A5%E5%BA%B7%E5%8F%91%E5%B8%83MedXIAOHE%E5%8C%BB%E7%96%97%E8%AF%84%E6%B5%8B%E5%9F%BA%E5%87%861.0.md)<br>
[浙大发布科研大模型求是引擎.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%B5%99%E5%A4%A7%E5%8F%91%E5%B8%83%E7%A7%91%E7%A0%94%E5%A4%A7%E6%A8%A1%E5%9E%8B%E6%B1%82%E6%98%AF%E5%BC%95%E6%93%8E.md)<br>
[全国首个农业气象灾害指数保险理赔自动化平台上线.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%85%A8%E5%9B%BD%E9%A6%96%E4%B8%AA%E5%86%9C%E4%B8%9A%E6%B0%94%E8%B1%A1%E7%81%BE%E5%AE%B3%E6%8C%87%E6%95%B0%E4%BF%9D%E9%99%A9%E7%90%86%E8%B5%94%E8%87%AA%E5%8A%A8%E5%8C%96%E5%B9%B3%E5%8F%B0%E4%B8%8A%E7%BA%BF.md)<br>
[国际空间站延寿至2032年多国确认继续合作.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%9B%BD%E9%99%85%E7%A9%BA%E9%97%B4%E7%AB%99%E5%BB%B6%E5%AF%BF%E8%87%B32032%E5%B9%B4%E5%A4%9A%E5%9B%BD%E7%A1%AE%E8%AE%A4%E7%BB%A7%E7%BB%AD%E5%90%88%E4%BD%9C.md)<br>
[国产三维近存AI芯片亮相.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%9B%BD%E4%BA%A7%E4%B8%89%E7%BB%B4%E8%BF%91%E5%AD%98AI%E8%8A%AF%E7%89%87%E4%BA%AE%E7%9B%B8.md)<br>
[工业旅游市场规模2029年破3000亿.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%B7%A5%E4%B8%9A%E6%97%85%E6%B8%B8%E5%B8%82%E5%9C%BA%E8%A7%84%E6%A8%A12029%E5%B9%B4%E7%A0%B43000%E4%BA%BF.md)<br>
[体育强国“十五五”规划发布.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%BD%93%E8%82%B2%E5%BC%BA%E5%9B%BD%E2%80%9C%E5%8D%81%E4%BA%94%E4%BA%94%E2%80%9D%E8%A7%84%E5%88%92%E5%8F%91%E5%B8%83.md)<br>
[广东警方打掉涉及多位顶流的MCN敲诈团伙.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%B9%BF%E4%B8%9C%E8%AD%A6%E6%96%B9%E6%89%93%E6%8E%89%E6%B6%89%E5%8F%8A%E5%A4%9A%E4%BD%8D%E9%A1%B6%E6%B5%81%E7%9A%84MCN%E6%95%B2%E8%AF%88%E5%9B%A2%E4%BC%99.md)<br>

[撞头赛车2足球版](https://www.xiazainiao.com/xiazai/74634.html) | [循迹讲堂app](https://www.xiazainiao.com/xiazai/74635.html) | [仙之炼金术师最新版](https://www.xiazainiao.com/xiazai/74636.html) | [厚学网app](https://www.xiazainiao.com/xiazai/74637.html) | [曲阜师范大学智慧曲园app最新版](https://www.xiazainiao.com/xiazai/74638.html) | [星际旅行游戏](https://www.xiazainiao.com/xiazai/74639.html) | [运动计步器](https://www.xiazainiao.com/xiazai/74640.html) | [物理演算建筑破坏游戏](https://www.xiazainiao.com/xiazai/74641.html) | [爱跑腿app](https://www.xiazainiao.com/xiazai/74642.html) | [NFT模拟器游戏](https://www.xiazainiao.com/xiazai/74643.html)

来源依据：
来源依据：[云冈石窟建成首套凝结水监测系统.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%BA%91%E5%86%88%E7%9F%B3%E7%AA%9F%E5%BB%BA%E6%88%90%E9%A6%96%E5%A5%97%E5%87%9D%E7%BB%93%E6%B0%B4%E7%9B%91%E6%B5%8B%E7%B3%BB%E7%BB%9F.md)<br>
[海洋二号E星发射组网海洋动力监测.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%B5%B7%E6%B4%8B%E4%BA%8C%E5%8F%B7E%E6%98%9F%E5%8F%91%E5%B0%84%E7%BB%84%E7%BD%91%E6%B5%B7%E6%B4%8B%E5%8A%A8%E5%8A%9B%E7%9B%91%E6%B5%8B.md)<br>
[中科院钙钛矿-有机叠层电池效率达28.04%.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%AD%E7%A7%91%E9%99%A2%E9%92%99%E9%92%9B%E7%9F%BF-%E6%9C%89%E6%9C%BA%E5%8F%A0%E5%B1%82%E7%94%B5%E6%B1%A0%E6%95%88%E7%8E%87%E8%BE%BE28.04%25.md)<br>
[我国成功发射可重复使用试验航天器.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%88%91%E5%9B%BD%E6%88%90%E5%8A%9F%E5%8F%91%E5%B0%84%E5%8F%AF%E9%87%8D%E5%A4%8D%E4%BD%BF%E7%94%A8%E8%AF%95%E9%AA%8C%E8%88%AA%E5%A4%A9%E5%99%A8.md)<br>
[壁仞科技NPO光互连超节点方案.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%A3%81%E4%BB%9E%E7%A7%91%E6%8A%80NPO%E5%85%89%E4%BA%92%E8%BF%9E%E8%B6%85%E8%8A%82%E7%82%B9%E6%96%B9%E6%A1%88.md)<br>
[城市宠物友好商场标准升温.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%9F%8E%E5%B8%82%E5%AE%A0%E7%89%A9%E5%8F%8B%E5%A5%BD%E5%95%86%E5%9C%BA%E6%A0%87%E5%87%86%E5%8D%87%E6%B8%A9.md)<br>
[NASA罗曼空间望远镜即将发射.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/NASA%E7%BD%97%E6%9B%BC%E7%A9%BA%E9%97%B4%E6%9C%9B%E8%BF%9C%E9%95%9C%E5%8D%B3%E5%B0%86%E5%8F%91%E5%B0%84.md)<br>
[公安部发布最新机动车和驾驶人数据.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%85%AC%E5%AE%89%E9%83%A8%E5%8F%91%E5%B8%83%E6%9C%80%E6%96%B0%E6%9C%BA%E5%8A%A8%E8%BD%A6%E5%92%8C%E9%A9%BE%E9%A9%B6%E4%BA%BA%E6%95%B0%E6%8D%AE.md)<br>
[平头哥真武M890+磐久AL128镇馆.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%B9%B3%E5%A4%B4%E5%93%A5%E7%9C%9F%E6%AD%A6M890%2B%E7%A3%90%E4%B9%85AL128%E9%95%87%E9%A6%86.md)<br>
[工信部加快算力标准体系+超节点白皮书.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%B7%A5%E4%BF%A1%E9%83%A8%E5%8A%A0%E5%BF%AB%E7%AE%97%E5%8A%9B%E6%A0%87%E5%87%86%E4%BD%93%E7%B3%BB%2B%E8%B6%85%E8%8A%82%E7%82%B9%E7%99%BD%E7%9A%AE%E4%B9%A6.md)<br>

[央视影音HD官方版](https://www.xiazainiao.com/xiazai/74644.html) | [aida64手机版](https://www.xiazainiao.com/xiazai/74645.html) | [aida64安卓版](https://www.xiazainiao.com/xiazai/74646.html) | [voa常速英语app](https://www.xiazainiao.com/xiazai/74647.html) | [异星特勤队安卓版](https://www.xiazainiao.com/xiazai/74648.html) | [浅言软件](https://www.xiazainiao.com/xiazai/74649.html) | [populele app](https://www.xiazainiao.com/xiazai/74650.html) | [populele智能尤克里里app](https://www.xiazainiao.com/xiazai/74651.html) | [我的打工日记游戏](https://www.xiazainiao.com/xiazai/74652.html) | [承管家app](https://www.xiazainiao.com/xiazai/74653.html)

来源依据：
来源依据：[zt_010_headline_ts_20260612.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/zt_010_headline_ts_20260612.md)<br>
[国内首个商业化地热能直接利用项目在雄安投运.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%9B%BD%E5%86%85%E9%A6%96%E4%B8%AA%E5%95%86%E4%B8%9A%E5%8C%96%E5%9C%B0%E7%83%AD%E8%83%BD%E7%9B%B4%E6%8E%A5%E5%88%A9%E7%94%A8%E9%A1%B9%E7%9B%AE%E5%9C%A8%E9%9B%84%E5%AE%89%E6%8A%95%E8%BF%90.md)<br>
[太空生物打印机在轨造出肝肾组织.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%A4%AA%E7%A9%BA%E7%94%9F%E7%89%A9%E6%89%93%E5%8D%B0%E6%9C%BA%E5%9C%A8%E8%BD%A8%E9%80%A0%E5%87%BA%E8%82%9D%E8%82%BE%E7%BB%84%E7%BB%87.md)<br>
[沙漠锁边林带实现机械化种植.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%B2%99%E6%BC%A0%E9%94%81%E8%BE%B9%E6%9E%97%E5%B8%A6%E5%AE%9E%E7%8E%B0%E6%9C%BA%E6%A2%B0%E5%8C%96%E7%A7%8D%E6%A4%8D.md)<br>
[《朝花夕拾》百年纪念版发布.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E3%80%8A%E6%9C%9D%E8%8A%B1%E5%A4%95%E6%8B%BE%E3%80%8B%E7%99%BE%E5%B9%B4%E7%BA%AA%E5%BF%B5%E7%89%88%E5%8F%91%E5%B8%83.md)<br>
[全国首个社区心理健康服务站全覆盖.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%85%A8%E5%9B%BD%E9%A6%96%E4%B8%AA%E7%A4%BE%E5%8C%BA%E5%BF%83%E7%90%86%E5%81%A5%E5%BA%B7%E6%9C%8D%E5%8A%A1%E7%AB%99%E5%85%A8%E8%A6%86%E7%9B%96.md)<br>
[浙江优化工商业分时电价政策七月起执行.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%B5%99%E6%B1%9F%E4%BC%98%E5%8C%96%E5%B7%A5%E5%95%86%E4%B8%9A%E5%88%86%E6%97%B6%E7%94%B5%E4%BB%B7%E6%94%BF%E7%AD%96%E4%B8%83%E6%9C%88%E8%B5%B7%E6%89%A7%E8%A1%8C.md)<br>
[深度求索自研推理芯片进入后端流片.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%B7%B1%E5%BA%A6%E6%B1%82%E7%B4%A2%E8%87%AA%E7%A0%94%E6%8E%A8%E7%90%86%E8%8A%AF%E7%89%87%E8%BF%9B%E5%85%A5%E5%90%8E%E7%AB%AF%E6%B5%81%E7%89%87.md)<br>
[全国暑期文旅消费季发4.5亿券.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%85%A8%E5%9B%BD%E6%9A%91%E6%9C%9F%E6%96%87%E6%97%85%E6%B6%88%E8%B4%B9%E5%AD%A3%E5%8F%914.5%E4%BA%BF%E5%88%B8.md)<br>
[zt_056_md_hybrid_batch2_20260617.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/zt_056_md_hybrid_batch2_20260617.md)<br>

[wifi万能钥匙显密码版](https://www.xiazainiao.com/xiazai/74654.html) | [WiFi万能钥匙显密码版2025](https://www.xiazainiao.com/xiazai/74655.html) | [wifi万能钥匙纯净版](https://www.xiazainiao.com/xiazai/74656.html) | [微软白板app\(Whiteboard\)](https://www.xiazainiao.com/xiazai/74657.html) | [像素生存Z汉化版](https://www.xiazainiao.com/xiazai/74658.html) | [舆情通app](https://www.xiazainiao.com/xiazai/74659.html) | [公主化妆世界手机版](https://www.xiazainiao.com/xiazai/74660.html) | [王权权力的游戏汉化版](https://www.xiazainiao.com/xiazai/74661.html) | [我是带货王最新版](https://www.xiazainiao.com/xiazai/74662.html) | [永不掉落安卓版](https://www.xiazainiao.com/xiazai/74663.html)

来源依据：
来源依据：[北极航道夏季通航时间延长至四个月.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%8C%97%E6%9E%81%E8%88%AA%E9%81%93%E5%A4%8F%E5%AD%A3%E9%80%9A%E8%88%AA%E6%97%B6%E9%97%B4%E5%BB%B6%E9%95%BF%E8%87%B3%E5%9B%9B%E4%B8%AA%E6%9C%88.md)<br>
[暑期档电影票房破56亿元.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%9A%91%E6%9C%9F%E6%A1%A3%E7%94%B5%E5%BD%B1%E7%A5%A8%E6%88%BF%E7%A0%B456%E4%BA%BF%E5%85%83.md)<br>
[ChinaCool带火入境深度游.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/ChinaCool%E5%B8%A6%E7%81%AB%E5%85%A5%E5%A2%83%E6%B7%B1%E5%BA%A6%E6%B8%B8.md)<br>
[植物基乳制品钙吸收率媲美牛奶.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%A4%8D%E7%89%A9%E5%9F%BA%E4%B9%B3%E5%88%B6%E5%93%81%E9%92%99%E5%90%B8%E6%94%B6%E7%8E%87%E5%AA%B2%E7%BE%8E%E7%89%9B%E5%A5%B6.md)<br>
[本届世界杯现场观众超650万创历史纪录.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%9C%AC%E5%B1%8A%E4%B8%96%E7%95%8C%E6%9D%AF%E7%8E%B0%E5%9C%BA%E8%A7%82%E4%BC%97%E8%B6%85650%E4%B8%87%E5%88%9B%E5%8E%86%E5%8F%B2%E7%BA%AA%E5%BD%95.md)<br>
[字节Seedance2.5支持30秒单次生成.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%AD%97%E8%8A%82Seedance2.5%E6%94%AF%E6%8C%8130%E7%A7%92%E5%8D%95%E6%AC%A1%E7%94%9F%E6%88%90.md)<br>
[中国科学家在量子计算纠错领域取得重大突破.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%AD%E5%9B%BD%E7%A7%91%E5%AD%A6%E5%AE%B6%E5%9C%A8%E9%87%8F%E5%AD%90%E8%AE%A1%E7%AE%97%E7%BA%A0%E9%94%99%E9%A2%86%E5%9F%9F%E5%8F%96%E5%BE%97%E9%87%8D%E5%A4%A7%E7%AA%81%E7%A0%B4.md)<br>
[上海暑期青少年体育夏令营报名火爆.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%8A%E6%B5%B7%E6%9A%91%E6%9C%9F%E9%9D%92%E5%B0%91%E5%B9%B4%E4%BD%93%E8%82%B2%E5%A4%8F%E4%BB%A4%E8%90%A5%E6%8A%A5%E5%90%8D%E7%81%AB%E7%88%86.md)<br>
[中科院上海光机所中红外连续激光光谱合束获进展.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%AD%E7%A7%91%E9%99%A2%E4%B8%8A%E6%B5%B7%E5%85%89%E6%9C%BA%E6%89%80%E4%B8%AD%E7%BA%A2%E5%A4%96%E8%BF%9E%E7%BB%AD%E6%BF%80%E5%85%89%E5%85%89%E8%B0%B1%E5%90%88%E6%9D%9F%E8%8E%B7%E8%BF%9B%E5%B1%95.md)<br>
[数字丝路发展论坛西安开幕.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%95%B0%E5%AD%97%E4%B8%9D%E8%B7%AF%E5%8F%91%E5%B1%95%E8%AE%BA%E5%9D%9B%E8%A5%BF%E5%AE%89%E5%BC%80%E5%B9%95.md)<br>

[电锯跷跷屋破解版\(see saw\)](https://www.xiazainiao.com/xiazai/74664.html) | [新年抢红包神器app](https://www.xiazainiao.com/xiazai/74665.html) | [BitWarden安卓版](https://www.xiazainiao.com/xiazai/74666.html) | [点心闹钟最新版](https://www.xiazainiao.com/xiazai/74667.html) | [全药通app](https://www.xiazainiao.com/xiazai/74668.html) | [鱼大大](https://www.xiazainiao.com/xiazai/74669.html) | [新免小说阅读器最新版](https://www.xiazainiao.com/xiazai/74670.html) | [东郊到家app](https://www.xiazainiao.com/xiazai/74671.html) | [全民烧脑3游戏](https://www.xiazainiao.com/xiazai/74672.html) | [海上鲜](https://www.xiazainiao.com/xiazai/74673.html)

来源依据：
来源依据：[横琴口岸7月客流车流双创历史新高.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%A8%AA%E7%90%B4%E5%8F%A3%E5%B2%B87%E6%9C%88%E5%AE%A2%E6%B5%81%E8%BD%A6%E6%B5%81%E5%8F%8C%E5%88%9B%E5%8E%86%E5%8F%B2%E6%96%B0%E9%AB%98.md)<br>
[浙大发布科研大模型求是引擎.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%B5%99%E5%A4%A7%E5%8F%91%E5%B8%83%E7%A7%91%E7%A0%94%E5%A4%A7%E6%A8%A1%E5%9E%8B%E6%B1%82%E6%98%AF%E5%BC%95%E6%93%8E.md)<br>
[zt_009_headline_bar_20260612.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/zt_009_headline_bar_20260612.md)<br>
[全国首个海洋碳汇交易平台在青岛上线.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%85%A8%E5%9B%BD%E9%A6%96%E4%B8%AA%E6%B5%B7%E6%B4%8B%E7%A2%B3%E6%B1%87%E4%BA%A4%E6%98%93%E5%B9%B3%E5%8F%B0%E5%9C%A8%E9%9D%92%E5%B2%9B%E4%B8%8A%E7%BA%BF.md)<br>
[山东7月下旬蚊虫密度达高风险级.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%B1%B1%E4%B8%9C7%E6%9C%88%E4%B8%8B%E6%97%AC%E8%9A%8A%E8%99%AB%E5%AF%86%E5%BA%A6%E8%BE%BE%E9%AB%98%E9%A3%8E%E9%99%A9%E7%BA%A7.md)<br>
[2026上海夏季音乐节以开拓者主题启幕.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/2026%E4%B8%8A%E6%B5%B7%E5%A4%8F%E5%AD%A3%E9%9F%B3%E4%B9%90%E8%8A%82%E4%BB%A5%E5%BC%80%E6%8B%93%E8%80%85%E4%B8%BB%E9%A2%98%E5%90%AF%E5%B9%95.md)<br>
[工业母机高精度数控系统突破封锁.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%B7%A5%E4%B8%9A%E6%AF%8D%E6%9C%BA%E9%AB%98%E7%B2%BE%E5%BA%A6%E6%95%B0%E6%8E%A7%E7%B3%BB%E7%BB%9F%E7%AA%81%E7%A0%B4%E5%B0%81%E9%94%81.md)<br>
[Costco入驻京东.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/Costco%E5%85%A5%E9%A9%BB%E4%BA%AC%E4%B8%9C.md)<br>
[SK海力士赴美IPO募资265亿美元.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/SK%E6%B5%B7%E5%8A%9B%E5%A3%AB%E8%B5%B4%E7%BE%8EIPO%E5%8B%9F%E8%B5%84265%E4%BA%BF%E7%BE%8E%E5%85%83.md)<br>
[景区AI抓拍影像付费引隐私讨论.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%99%AF%E5%8C%BAAI%E6%8A%93%E6%8B%8D%E5%BD%B1%E5%83%8F%E4%BB%98%E8%B4%B9%E5%BC%95%E9%9A%90%E7%A7%81%E8%AE%A8%E8%AE%BA.md)<br>

[愤怒的小球最新版](https://www.xiazainiao.com/xiazai/74674.html) | [羚羊夫人的幼儿园游戏](https://www.xiazainiao.com/xiazai/74675.html) | [Angry Birds 2](https://www.xiazainiao.com/xiazai/74676.html) | [游戏藏起来了3\(隐藏我的游戏3\)](https://www.xiazainiao.com/xiazai/74677.html) | [江苏人才网app](https://www.xiazainiao.com/xiazai/74678.html) | [轻啦app](https://www.xiazainiao.com/xiazai/74679.html) | [免费淘小说app](https://www.xiazainiao.com/xiazai/74680.html) | [赚钱帮app](https://www.xiazainiao.com/xiazai/74681.html) | [图片文档识别OCR](https://www.xiazainiao.com/xiazai/74682.html) | [异世山河幻想破解版](https://www.xiazainiao.com/xiazai/74683.html)

来源依据：
来源依据：[上汽西班牙建厂首批700辆运抵.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%8A%E6%B1%BD%E8%A5%BF%E7%8F%AD%E7%89%99%E5%BB%BA%E5%8E%82%E9%A6%96%E6%89%B9700%E8%BE%86%E8%BF%90%E6%8A%B5.md)<br>
[柔性电子皮肤实现触觉反馈闭环.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%9F%94%E6%80%A7%E7%94%B5%E5%AD%90%E7%9A%AE%E8%82%A4%E5%AE%9E%E7%8E%B0%E8%A7%A6%E8%A7%89%E5%8F%8D%E9%A6%88%E9%97%AD%E7%8E%AF.md)<br>
[rj_033_html_compact_20260617.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/rj_033_html_compact_20260617.md)<br>
[台风红霞残涡影响河南发布农田渍涝预警.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%8F%B0%E9%A3%8E%E7%BA%A2%E9%9C%9E%E6%AE%8B%E6%B6%A1%E5%BD%B1%E5%93%8D%E6%B2%B3%E5%8D%97%E5%8F%91%E5%B8%83%E5%86%9C%E7%94%B0%E6%B8%8D%E6%B6%9D%E9%A2%84%E8%AD%A6.md)<br>
[国家市场监管总局部署打击劣质低价专项行动.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%9B%BD%E5%AE%B6%E5%B8%82%E5%9C%BA%E7%9B%91%E7%AE%A1%E6%80%BB%E5%B1%80%E9%83%A8%E7%BD%B2%E6%89%93%E5%87%BB%E5%8A%A3%E8%B4%A8%E4%BD%8E%E4%BB%B7%E4%B8%93%E9%A1%B9%E8%A1%8C%E5%8A%A8.md)<br>
[新版国家基本药物目录时隔八年更新发布.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%96%B0%E7%89%88%E5%9B%BD%E5%AE%B6%E5%9F%BA%E6%9C%AC%E8%8D%AF%E7%89%A9%E7%9B%AE%E5%BD%95%E6%97%B6%E9%9A%94%E5%85%AB%E5%B9%B4%E6%9B%B4%E6%96%B0%E5%8F%91%E5%B8%83.md)<br>
[人工光合系统实现二氧化碳直接合成淀粉前体.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%BA%BA%E5%B7%A5%E5%85%89%E5%90%88%E7%B3%BB%E7%BB%9F%E5%AE%9E%E7%8E%B0%E4%BA%8C%E6%B0%A7%E5%8C%96%E7%A2%B3%E7%9B%B4%E6%8E%A5%E5%90%88%E6%88%90%E6%B7%80%E7%B2%89%E5%89%8D%E4%BD%93.md)<br>
[均普智能WAIC展出六机器人BMS协同产线.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%9D%87%E6%99%AE%E6%99%BA%E8%83%BDWAIC%E5%B1%95%E5%87%BA%E5%85%AD%E6%9C%BA%E5%99%A8%E4%BA%BABMS%E5%8D%8F%E5%90%8C%E4%BA%A7%E7%BA%BF.md)<br>
[孙颖莎4比3险胜蒯曼夺得WTT美国大满贯女单冠军.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%AD%99%E9%A2%96%E8%8E%8E4%E6%AF%943%E9%99%A9%E8%83%9C%E8%92%AF%E6%9B%BC%E5%A4%BA%E5%BE%97WTT%E7%BE%8E%E5%9B%BD%E5%A4%A7%E6%BB%A1%E8%B4%AF%E5%A5%B3%E5%8D%95%E5%86%A0%E5%86%9B.md)<br>
[世界杯扩军后非洲球队整体表现亮眼.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%96%E7%95%8C%E6%9D%AF%E6%89%A9%E5%86%9B%E5%90%8E%E9%9D%9E%E6%B4%B2%E7%90%83%E9%98%9F%E6%95%B4%E4%BD%93%E8%A1%A8%E7%8E%B0%E4%BA%AE%E7%9C%BC.md)<br>

[旋转动物园中文版](https://www.xiazainiao.com/xiazai/74684.html) | [一刻相册app](https://www.xiazainiao.com/xiazai/74685.html) | [渝小就app](https://www.xiazainiao.com/xiazai/74686.html) | [奇妙餐厅破解版](https://www.xiazainiao.com/xiazai/74687.html) | [YouCam Perfect](https://www.xiazainiao.com/xiazai/74688.html) | [外研通app](https://www.xiazainiao.com/xiazai/74689.html) | [艾塔纪元国际服最新版](https://www.xiazainiao.com/xiazai/74691.html) | [番茄快搜app](https://www.xiazainiao.com/xiazai/74692.html) | [今日影视app](https://www.xiazainiao.com/xiazai/74693.html) | [卡通战争](https://www.xiazainiao.com/xiazai/74694.html)

来源依据：
来源依据：[城市噪声污染源头治理强化.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%9F%8E%E5%B8%82%E5%99%AA%E5%A3%B0%E6%B1%A1%E6%9F%93%E6%BA%90%E5%A4%B4%E6%B2%BB%E7%90%86%E5%BC%BA%E5%8C%96.md)<br>
[减肥针停药半年体重反弹超八成.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%87%8F%E8%82%A5%E9%92%88%E5%81%9C%E8%8D%AF%E5%8D%8A%E5%B9%B4%E4%BD%93%E9%87%8D%E5%8F%8D%E5%BC%B9%E8%B6%85%E5%85%AB%E6%88%90.md)<br>
[全球粮食安全指数发布多国面临严峻挑战.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%85%A8%E7%90%83%E7%B2%AE%E9%A3%9F%E5%AE%89%E5%85%A8%E6%8C%87%E6%95%B0%E5%8F%91%E5%B8%83%E5%A4%9A%E5%9B%BD%E9%9D%A2%E4%B8%B4%E4%B8%A5%E5%B3%BB%E6%8C%91%E6%88%98.md)<br>
[中国数学家邓煜、王虹获菲尔兹奖.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%AD%E5%9B%BD%E6%95%B0%E5%AD%A6%E5%AE%B6%E9%82%93%E7%85%9C%E3%80%81%E7%8E%8B%E8%99%B9%E8%8E%B7%E8%8F%B2%E5%B0%94%E5%85%B9%E5%A5%96.md)<br>
[上半年新能源汽车出口235.5万辆翻1.2倍.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%B8%8A%E5%8D%8A%E5%B9%B4%E6%96%B0%E8%83%BD%E6%BA%90%E6%B1%BD%E8%BD%A6%E5%87%BA%E5%8F%A3235.5%E4%B8%87%E8%BE%86%E7%BF%BB1.2%E5%80%8D.md)<br>
[AI进校园多地中小学建智慧实验室.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/AI%E8%BF%9B%E6%A0%A1%E5%9B%AD%E5%A4%9A%E5%9C%B0%E4%B8%AD%E5%B0%8F%E5%AD%A6%E5%BB%BA%E6%99%BA%E6%85%A7%E5%AE%9E%E9%AA%8C%E5%AE%A4.md)<br>
[天问二号成功交会小行星2016HO3.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%A4%A9%E9%97%AE%E4%BA%8C%E5%8F%B7%E6%88%90%E5%8A%9F%E4%BA%A4%E4%BC%9A%E5%B0%8F%E8%A1%8C%E6%98%9F2016HO3.md)<br>
[全国首个海洋碳汇交易平台在青岛上线.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%85%A8%E5%9B%BD%E9%A6%96%E4%B8%AA%E6%B5%B7%E6%B4%8B%E7%A2%B3%E6%B1%87%E4%BA%A4%E6%98%93%E5%B9%B3%E5%8F%B0%E5%9C%A8%E9%9D%92%E5%B2%9B%E4%B8%8A%E7%BA%BF.md)<br>
[公路咖啡创业持续走红.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%85%AC%E8%B7%AF%E5%92%96%E5%95%A1%E5%88%9B%E4%B8%9A%E6%8C%81%E7%BB%AD%E8%B5%B0%E7%BA%A2.md)<br>
[优刻得×上理太空算力地面样机.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E4%BC%98%E5%88%BB%E5%BE%97%C3%97%E4%B8%8A%E7%90%86%E5%A4%AA%E7%A9%BA%E7%AE%97%E5%8A%9B%E5%9C%B0%E9%9D%A2%E6%A0%B7%E6%9C%BA.md)<br>


---

**来源参考：**
- [Anthropic发布ClaudeOpus5.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/Anthropic%E5%8F%91%E5%B8%83ClaudeOpus5.md)
- [rj_038_md_hybrid_20260617.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/rj_038_md_hybrid_20260617.md)
- [台风巴威逼近东南沿海多地启动应急响应.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%8F%B0%E9%A3%8E%E5%B7%B4%E5%A8%81%E9%80%BC%E8%BF%91%E4%B8%9C%E5%8D%97%E6%B2%BF%E6%B5%B7%E5%A4%9A%E5%9C%B0%E5%90%AF%E5%8A%A8%E5%BA%94%E6%80%A5%E5%93%8D%E5%BA%94.md)
- [zt_003_headline_bar_20260612.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/zt_003_headline_bar_20260612.md)
- [2026AGIC深圳国际AI大会定档8月26日.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/2026AGIC%E6%B7%B1%E5%9C%B3%E5%9B%BD%E9%99%85AI%E5%A4%A7%E4%BC%9A%E5%AE%9A%E6%A1%A38%E6%9C%8826%E6%97%A5.md)
- [zt_045_html_std_20260617.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/zt_045_html_std_20260617.md)
- [协和等完成亚洲首个肺结节AI良恶性鉴别临床试验.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%8D%8F%E5%92%8C%E7%AD%89%E5%AE%8C%E6%88%90%E4%BA%9A%E6%B4%B2%E9%A6%96%E4%B8%AA%E8%82%BA%E7%BB%93%E8%8A%82AI%E8%89%AF%E6%81%B6%E6%80%A7%E9%89%B4%E5%88%AB%E4%B8%B4%E5%BA%8A%E8%AF%95%E9%AA%8C.md)
- [央行延续适度宽松货币政策加大逆周期调节.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%A4%AE%E8%A1%8C%E5%BB%B6%E7%BB%AD%E9%80%82%E5%BA%A6%E5%AE%BD%E6%9D%BE%E8%B4%A7%E5%B8%81%E6%94%BF%E7%AD%96%E5%8A%A0%E5%A4%A7%E9%80%86%E5%91%A8%E6%9C%9F%E8%B0%83%E8%8A%82.md)
- [数字丝路发展论坛西安开幕.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E6%95%B0%E5%AD%97%E4%B8%9D%E8%B7%AF%E5%8F%91%E5%B1%95%E8%AE%BA%E5%9D%9B%E8%A5%BF%E5%AE%89%E5%BC%80%E5%B9%95.md)
- [小米人形机器人进汽车工厂螺母工位点.md](https://github.com/ww8642199-svg/daily-news-zt12/blob/main/%E5%B0%8F%E7%B1%B3%E4%BA%BA%E5%BD%A2%E6%9C%BA%E5%99%A8%E4%BA%BA%E8%BF%9B%E6%B1%BD%E8%BD%A6%E5%B7%A5%E5%8E%82%E8%9E%BA%E6%AF%8D%E5%B7%A5%E4%BD%8D%E7%82%B9.md)