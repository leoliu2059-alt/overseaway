# SEO（第1-24篇）

## 图片也能做 SEO
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247483850&idx=1&sn=1a467ecb81a2ff6a2e4ed83b248e034f&chksm=c28d2591f5faac8768d7f3b5c4e52fc78edbe4ede2d7f9801f1d502b75902138a6700355ded4#rd
- 详情：图片搜索是用户常见的搜索意图之一，若网站拥有匹配的高质量图片，就能出现在 Google 图片搜索结果首屏，从而获得额外入口。方法论：①每个页面/功能尽量放一张"大图"，长边至少 1000px 以上，避免只放 200×300 的小图，模糊图会损害体验；②写好 alt 文本，与内容相关，这是图片在搜索关键字排名的关键；③文件名也要与图片语义相关（如 nano-banana-poster.png），补充语义信号。案例：nano banana poster 爆火时，flux ai 因提供一张高清图就多了一个网站入口。工具/要点：alt 属性 + 语义化文件名 + 高分辨率原图，三者结合即可吃图片搜索流量。

## 避免无关词影响核心关键词
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247483898&idx=1&sn=b57b7dad3b4619ab791237e9f0127604&chksm=c28d25a1f5faacb7a7b0a4fedfe8d34688785461b6f4c34fb76b6cda159926c9c42e47d2e499#rd
- 详情：页面中无关按钮文字会污染核心关键词密度。案例：某页面因一个 "apply configuration" 按钮，使该词成为关键词密度最大的词，严重影响 SEO。解决方法：用 CSS content 渲染装饰性/固定文字，避免进入 HTML 文本节点被爬虫统计。操作步骤：在 React 组件中设 CSS 变量（如 --play-text），再于 CSS 用 ::after { content: var(--play-text); } 输出；其中文本仍取自国际化函数 ${t('play')}，保证多语言适配不破坏。效果：不影响多语言，又避免大量重复无关词稀释核心词权重。要点：装饰性文字、按钮标签尽量通过 CSS 伪元素注入，核心关键词密度才能集中在正文中。

## 多平台收录网站
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484000&idx=1&sn=62aeffbaa73d5174bbb486e59460c983&chksm=c28d263bf5faaf2d8c921db6bd373d12944c441d583c87f2e0327899f7d4f25ae7ca5af58614#rd
- 详情：多平台提交站点地图可拓展流量来源。需提交的搜索引擎站长平台：Google Search Console（search.google.com/search-console，全球最大）、Bing Webmaster（www.bing.com/webmasters）、Naver（searchadvisor.naver.com，韩国必备）、Yandex（webmaster.yandex.com，俄语区重要）；国内：百度（ziyuan.baidu.com/linksubmit/url）、360（zhanzhang.so.com）、搜狗（zhanzhang.sogou.com）。配置要点：除 Google 不完全依赖 Sitemap 外，其余平台省钱地收录较依赖站长主动提交 Sitemap。额外技巧：Cloudflare 中开启 域名→缓存→配置→Crawler Hints，可让其他网站自动被收录。方法论：提交即获得更多索引入口，是低成本获取多区域流量的基础动作。

## 搜索引擎爬虫访问说明书
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484063&idx=1&sn=a5873adb1e82394e291a3cf92027968b&chksm=c28d26c4f5faafd265ce70e8f5be74e2951491784dd36acb1f8ccd142ffaaa1023c65f2b51f4#rd
- 详情：robots.txt 是网站对所有搜索引擎爬虫的"访问说明书"，爬虫访问前会先读取它决定抓取范围。标准写法示例：User-agent:*（对所有爬虫生效）、Disallow:/admin/（禁止爬后台）、Allow:/（其余可访问）、Sitemap:https://example.com/sitemap.xml（告知地图位置）。作用：①控制爬虫范围，避免 /login、/cart、/api、测试页被无意义抓取；②提升 SEO 效率——搜索引擎抓取预算有限，别浪费在无效页；③保护隐私与安全，防敏感接口被爬；④提供 sitemap 入口。与 sitemap 区别：robots.txt 是"门卫"控制访问，sitemap.xml 是"导游"指路，二者配合效果最佳。

## semrush 查看主要页面
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484131&idx=1&sn=33865e2a05d9ebc7c29c1d44cc0a5b3a&chksm=c28d26b8f5faafaedeeee58dfde5e8a5f64dd41c49d3577e2ff6d20919a4b36c8c38f66b60ef#rd
- 详情：用 Semrush 的"主要页面（Top Pages）"功能可查看竞品各页面的流量分布，是竞品 SEO 拆解的核心手段。操作步骤：进入 Semrush→流量与市场（Traffic & Market）→输入目标域名（如 pollo.ai）→切换到"主要页面"标签→按"自然流量"排序查看。案例：pollo.ai 的 SEO 做得好，视频相关关键词、视频特效等都有自然流量。方法论：找到这些有流量的页面后，可用"加精品内页"打法复刻同类页面；同时能发现近期飙升的新需求。要点：关注自然流量指标排序，既能找可抄的页面模板，又能捕捉新兴需求信号。

## sitemap 使用小技巧
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484144&idx=1&sn=73c9883ec4f20210845c74ffaa8f96fb&chksm=c28d26abf5faafbd71f7f9b6519a96b15e84b962b62405f60237c449a8b21767f437c42e5621#rd
- 详情：Sitemap（网站地图）告诉搜索引擎网站有哪些页面，辅助智能抓取。常规用法：在 GSC 提交站点地图让其索引。进阶玩法：利用 sitemap 监控新游戏/新词上线。步骤：①用 AI 写脚本记录历史 sitemap 快照；②在服务器放定时任务，每天爬取目标站（尤其是反应快的新站、竞品站）sitemap；③对比变化，通知你新增了哪些内页、用了哪些长尾新词。方法论：监控竞品 sitemap 可发现其上新内页与长尾词布局，从而快速跟进。实现简单——留存旧 sitemap 与今日对比即可，是低成本的需求探测与竞品跟踪手段。

## 低竞争小词的魅力，8 条外链拿下 41K 的月访问量
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484215&idx=1&sn=5bca516f41ac7ae3e63b9930cf9dba92&chksm=c28d276cf5faae7a4ebf21fb24f7339cafe31961ecf4b49e9a805e3c05d09b2b4bcd94feb8dd#rd
- 详情：挖掘到一个低竞争新词 openai fm 的网站，无功能只有 YouTube 演示视频，仅 8 条外链、KD 为 0，却在 Google 排第二、拿下 41K 月访问量。验证工具：backlink-checker（看外链仅 8 条、KD 0）、aitdk（查域名 3 月注册、60% 流量来自搜索）、allintitle:openai fm（标题含该词的网站仅 1220 个）。页面结构：顶部跳转按钮→官网，下方 YouTube 视频增加停留时长，另写博客为 Adsense 过审并保持新鲜度。发现方法：朴素"词根找词"——以 openai 为词根在 Google Trends 相关搜索找到该词。要点：低竞争新词竞争对手少、需求真实，不卷也能拿排名，但上限不高。

## 这个插件让你快速找词
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484222&idx=1&sn=343b5c69e3d6523ffa2f71ce5d77a135&chksm=c28d2765f5faae73f533202389662cbc2618614612f35481c4b4dedf30ae7b5085a799506ef4#rd
- 详情：推荐 Chrome 插件 Google Trends Everywhere（商店地址 lkjapnejglpmnnpljfnnpndjbbopddge）。用法一：基于你的搜索词，快速查看其他网站在该词下的 top 关键词，实现"词找词"扩展。用法二：平时浏览社媒或看到任意词时，选中该词→右键即可快速查看对应的 Google 趋势数据。方法论：把趋势查询融入日常浏览，随时发现热点与需求词，配合词根找词效率极高。要点：这是轻量、即时的关键词发现工具，适合在刷信息流时顺手挖掘新词，无需打开独立后台。

## 搜索引擎思维做网站
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484297&idx=1&sn=8edf1f1b05565ce26f27c538c2e25757&chksm=c28d27d2f5faaec48c8a9a9aaa1d68b35938bcc147301962bb647ba77a327d4827583bd63c21#rd
- 详情：当网站页面膨胀到海量级别时，你自身就是个小型搜索引擎，要扮演好生态平台角色——定制规则，让好内容快速触达用户、差内容下沉。方法论（新陈代谢机制）：①对长期（数月）无流量的页面做淘汰，去掉入口内链、移出 Sitemap；②保持有新增也有淘汰，让 Google 和用户都更快触达好内容；③因爬虫预算（crawl budget）有限，网站设计时要对大量内链做判断，决定给不给入口链接。要点：用搜索引擎的取舍逻辑运营自己的站内权重分配，把有限抓取预算集中到优质页面，是大型站 SEO 的核心思维。

## 手动请求索引加快收录速度
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484351&idx=1&sn=adb05eaf75cba1cbb19aa2e4754a756d&chksm=c28d27e4f5faaef207bfb16371ba6cac691d8cc317795f8df3a0b00f5dcfd86afc8bddaa8b51#rd
- 详情：作者一次添加 10 来个多语言页面、sitemap 新增 6 个页面，手动请求索引后发现：手动申请的页面收录更快，未手动操作的暂不收录。结论：适配多语言或新页面上线时，尽量逐页手动申请一次索引以加速收录。操作步骤（在 GSC）：①输入框输入域名，按回车搜索；②先点左侧"测试"按钮，再点"请求编入索引"。要点：这是低成本、高确定性的收录加速手段，尤其适合多语言批量上线场景，逐页操作比单纯等 sitemap 抓取更可控。

## 查看网站 DR 神器
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484359&idx=1&sn=6aaf68a66c017f092423b9f30c01ba1d&chksm=c28d279cf5faae8af107b2dfb4a6ce718109f2092daba3fca5ac798e567d056de324536a1403#rd
- 详情：推荐 ahrefs 出品的 SEO Toolbar 浏览器插件（商店地址 hgmoccdbjhknikckedaaebbpdeebhiei）。最大亮点：安装后直接在浏览器图标上实时显示当前网站的 DR（域名评级），无需任何额外操作。其余功能与 AITDK 类似（展示形式有别），可通过侧边栏选项查看各项 SEO 数据。方法论：DR 是评估网站外链权重的关键指标，浏览竞品/目标站时一眼看 DR，便于快速判断其权威度与竞争难度。要点：把权重查看嵌入日常浏览，省去打开工具后台的麻烦。

## SEO 问题一键扫描
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484397&idx=1&sn=9e8d0ee2227bfeafd4247610ae81c7c8&chksm=c28d27b6f5faaea0c8669d3844ceefb2d9f777df1e5798858fafa08f106cca20807dd7671d34#rd
- 详情：推荐 Bing 的 SEO 问题扫描工具（www.bing.com/webmasters/sitescan）。操作步骤：①打开网址，若未在 Bing 提交收录，需先提交（可从 Google Search Console 直接导入）；②选择 Site Scan→Start New Scan，填写网站基本信息开始扫描；③扫描需等待，成功后即可在该路径下查看扫描出的 SEO 问题。案例：作者扫描 23 个页面发现 11 个问题，能定位可优化的具体点。方法论：定期一键扫描可系统化发现站内 SEO 缺陷，比人工排查更高效。要点：Bing 站长工具免费提供，适合做常态化 SEO 体检。

## 利用 youtube 生成内页，增加搜索流
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484403&idx=1&sn=d72deaa6b4bb3f3db45bc7c5a00ee098&chksm=c28d27a8f5faaebed237fbffaf7c87dfa7c53dfd854c4ebbd20595f21d911501ed5c539d72f0#rd
- 详情：把 YouTube 优质视频的字幕提取成内页文案，可带来搜索流量。工具一：Chrome 插件 youtube-transcript（jgibaoklabopileepldnlkbbcibhbgmd），观看视频时右侧直接提取全部字幕；工具二：GitHub 库 youtube-transcript-api（jdepoix/youtube-transcript-api）可代码集成。操作：让 Claude Code 处理"视频链接 xxx 帮我把详细文稿整理出来"。作用：把博主优质文案作为网页内容+嵌入视频，既是一手优质内容、提升收录，视频配合文案还增强观看体验、增加停留时长。要点：抢占新视频（如 sora 2 讲解）的上线速度，快人一步做成内页即可吃时效流量。

## 多语言适配
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484410&idx=1&sn=bb28ee6dd26f7d2458e5ca3ff967e679&chksm=c28d27a1f5faaeb7c9a496aff8504a5a3e5b93c6d5267123fb789a2b42c2984bd807b91820eb#rd
- 详情：多语言国家的适配策略。步骤：①新站先只做英文，减少问题、快速上站，新词新站先发优势大；②再适配主流发达国家，可让 ChatGPT 基于网站类型推荐优先语言；③基于 GSC 访问数据看各国流量，按需适配。关键词方法：用工具找到该语言下有流量的核心关键词，再让 AI 基于核心词+英文原文翻译，保证 SEO 与本地语感。关键提醒：不要一次提交多个多语言（内页多+多语言=页面暴增），易被 Google 判批量自动化上页而 K 站；作者每次只上一两个，等 GSC 收录再继续；并配置 hreflang 告诉 Google 这是多语言而非复制内容。

## 多语言自动检测提醒
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484431&idx=1&sn=407aeddebd648d465bfde202ccd41072&chksm=c28d2054f5faa942c2e725f937265987c717064c76f3ceaf53222c3c85b620a37629cbfae068#rd
- 详情：做了多语言但若需用户手动切换，会损转化率（作者表情包站默认英文、中文用户看不懂而流失）。方案：基于用户 IP 自动提醒切换。实现：服务端请求 ipapi.co/json 或 ipinfo.io/json（有免费额度）拿到国家代码，弹出"检测到您在 xx，是否切换为 xx 语言"；若用户曾切换过，前端记录其选择并优先采用。注意（群友提醒）：自动切换可能影响爬虫与收录——若 Google 正爬中文页却被切到英文，会取不到对应页面数据。要点：用 IP 提示而非强制跳转，兼顾转化与 SEO 收录安全。

## 蹭词的新玩法
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484443&idx=1&sn=fd6d03418a0c7fbaf4f3faa144ce22f2&chksm=c28d2040f5faa956750db93bb50021d8a6708080716ab979267cc77caae76ac95b42cb247460#rd
- 详情：蹭新词的新玩法——直接给自有品牌站导流。传统蹭词靠订阅/广告，需支付或 Adsense 审核；新玩法是注册热门新词域名（如 gemini 3 爆火时 gemini3.com 给 YouWare 引流）把流量导给自己品牌站。步骤：①追当下热门新词抢注域名；②页面给品牌站导流（有积累）；③若无品牌站，可用联盟营销给别站引流赚佣；④若词持续火热，再独立做订阅等。要点：蹭新词=一波大流量，且给品牌站引流是长期积累；专业玩家已用此手法追新词，建议普通站长也跟进。

## 截流
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484489&idx=1&sn=f6222a8cb28c3e41403fb8660e9cae0c&chksm=c28d2012f5faa9044b5762755a7a650fb051ec110112981709bc85cac286a9a7d4ebcd412ec4#rd
- 详情：截流与防截流。很多模型词是在截大厂流量；案例：小排老师发 morisot.ai 后立刻有人抢注相关域名，其 Raphael 盗版流量甚至高于正版，作者最初也误入盗版。防被截流：①尽量别在全是竞争者的地方公布产品；②确保搜索你的品牌词时你排第一，否则口碑/红人带来的品牌搜索流量会拱手让人。进攻玩法：投流竞品的品牌词——搜竞品词的用户需求精准、CPC 可能更低；同时自己也要投自身品牌词提升权重。要点：品牌词排名防御 + 竞品品牌词投流，是截流攻防的两端。

## 布局 AI 搜索
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484526&idx=1&sn=1bdf3fb20abb23ca61c72d0ba0cda9d6&chksm=c28d2035f5faa92313abdaf720800f046032cb8fb51ea0a461a3893dc8a5e7817d31cadebfbd#rd
- 详情：ChatGPT 来的用户付费率高，值得布局 GEO（生成式引擎优化）。心得：①SEO 做得好，AI 联网搜索时能搜到你，GEO 自然不错；②站在用户角度问 GPT 推荐产品，开启 thinking 模式看它在哪搜索、搜了什么词，据此布局对应搜索词让网站被搜到；③在它搜索的来源处提交外链，增加被检索到的概率。要点：GEO 本质是 SEO 的延伸——把内容铺到 AI 会去检索的来源（网页+外链），让推荐结果包含你的站，核心仍是可被检索与权威度。

## 图片优化
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484561&idx=1&sn=0bca74e663ca01684e41f4a5fd7e8601&chksm=c28d20caf5faa9dc710c4a99148e3f63c8f64a6aa73d713b5ca1765f3e0d666efd6f4948be6b#rd
- 详情：图片优化兼顾加载速度与 SEO。步骤：①用 webp 格式（压缩体积小）；②非大图展示则缩减尺寸；③用 iloveimg、tinypng 压缩/调尺寸，或让 Claude Code 直接压缩转格式；④懒加载——<img> 加 loading="lazy"，屏外图滚动到才加载；⑤用 Cloudflare 等 CDN 存储加速访问。图片 SEO：加有意义 alt 文本、文件名改有意义英文，让图片有机会在相关搜索词下展示。要点：图片优化是"速度+SEO"双收益动作，webp+懒加载+CDN 三件套能明显提升核心网页指标与图片搜索曝光。

## SEO 插件分享
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484569&idx=1&sn=1349546b3162db9ba81bad7cb3a0bc12&chksm=c28d20c2f5faa9d46a35f17d534b949bb7e9c9e8bf16f5dfb0db13a04429d584ceb0b549d84d#rd
- 详情：推荐 Chrome 插件 sitedata（商店地址 emeakbgdecgmdjgegnejpppcnkcnoaen）。功能：在 Google 搜索结果页直接查看任意站的流量情况、网页基本信息、域名信息、导流搜索词。进阶反查：①通过 Google Ads 投流反查，找到该网站所有投流者及其投流的网站；②通过 Google Adsense 反查，查某人的所有接入 Adsense 的网站。方法论：这是竞品调研利器——既能看流量规模，又能顺藤摸瓜挖出投流网络与站群关系。要点：把流量/投流/域名情报前置到搜索结果页，调研效率极高。

## 搜索语法找外链
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484576&idx=1&sn=ead689fec682756994d72df12319c91b&chksm=c28d20fbf5faa9ed0cad67e7ae00db4fb2d1cc27516a94f04b22ebcf7e130b45d7a24a9bdb09#rd
- 详情：用 Google 搜索语法找外链。语法基础：intext 在正文找内容、site 限定某站、-site 排除某站。找某站外链=全网正文提到它但非它自己，以 pollo.ai 为例：intext:pollo.ai -site:pollo.ai。若想看某站如何发外链，可限定平台，如 intext:pollo.ai site:reddit.com。方法论：用 intext+排除自身域名，可批量发现谁在给你/竞品做外链；叠加 site 可定位特定平台（reddit 等）的外链发布模式。要点：零成本的外链侦察法，适合监测竞品外链来源与自身被引情况。

## ahrefs SEO 免费工具
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484607&idx=1&sn=3fbb94c0500110f80596fa7383e6fb7e&chksm=c28d20e4f5faa9f21fa0376f035597593e0bbf17b26d9c29dea0d0cbf1925e1516171b652a47#rd
- 详情：整理 ahrefs 的免费 SEO 工具集。常用：①网站流量查询 traffic-checker；②关键词难度查询 keyword-difficulty；③关键词生成器 keyword-generator；④外链查询 backlink-checker。更多免费工具在 ahrefs.com/free-seo-tools 页面下拉选择。方法论：这些免费版可替代部分付费功能做日常侦查——查流量规模、估 KD 难度、扩词、看外链。要点：ahrefs 免费工具足够支撑关键词挖掘、难度评估与外链监测的入门需求，无需立刻付费。

## typo 词的妙用
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484634&idx=1&sn=1acf3b1e20e1fcb440cadce095ece50e&chksm=c28d2081f5faa997b3e75e491378e0ff8625a712b5aa1280265e331aaf99fe13ed622d686e9d#rd
- 详情：typo 词是用户搜索时的拼写错误词（如 chatgpt→catgpt，nano banana→nana banana），其搜索量有时甚至超主词。用法：①注册 typo 词域名蹭品牌且无品牌风险、竞争更小，案例 nana banana 晚注册半月仍拿流量，nanabanana ai/io 域名甚至拿到 544k 流量；②布局关键字，因竞争小易排名；③投广告试 typo 词，主词被盯死而 typo 词关注少、单价更低、需求相同。要点：typo 词是低竞争、高性价比的词策略，可同时用于域名抢注、SEO 内页与广告投放。

## Canonical 标签
- 链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg%3D%3D&mid=2247484652&idx=1&sn=9eacfd1d6f4bd003a2d1b5c3e2f015fe&chksm=c28d20b7f5faa9a102794307478c640e3cc87acb6b05651dfc0f4007fa502a57167f1318b7af#rd
- 详情：Canonical 标签告诉搜索引擎哪个 URL 是规范版本，避免相同内容在多个 URL 被重复索引；若不正确，可能分散链接权重甚至降权。常见误区：以为自己无参数就不需要——但三方来源会默认加参数（如来自 chatgpt 会带 utm_source=chatgpt.com），仍需 canonical 指明规范页。操作：用 AITDK 插件查看页面 canonical 是否与 URL 一致；建议固定格式（如统一无 www、统一 / 结尾），后续发外链也保持统一，避免混淆。要点：canonical 是权重归集的基础配置，统一规范 URL 格式能防止参数页稀释主页面权重。
