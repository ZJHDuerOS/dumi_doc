## 新闻返回示例:

```javascript
// 播放娱乐新闻
{
    "data": {
        "directives": [
            {
                "header": {
                    "namespace": "SpeechSynthesizer",
                    "name": "Speak",
                    "message_id": "1487828738_637887xkx"
                },
                "payload": {
                    "token": "3020804145379379001",
                    "type": "Text",
                    "speak_behavior": "REPLACE_ALL",
                    "content": [
                        "华谊兄弟的贺岁电影之路",
                        "最初的贺岁档从12月中下旬延伸至1月上旬，但由于众多等候上映的影片和庞大的观影消费需求，贺岁档的时间跨度也明显增长，如今在广义上一般认为从每年11月第三个周末起、至次年3月初的电影档期，都属于“贺岁档”",
                        "作为中国大陆最知名的综合性娱乐集团，1998年华谊兄弟正式进入影视界开发、制作及发行中国最受欢迎的影视作品，为中国贺岁电影档贡献了诸多口碑佳作，为观众们创造了一段段经典的银幕回忆"
                    ],
                    "should_get_next_speech": true
                }
            }
        ],
        "speech": {
            "type": "Text",
            "content": ""
        },
        "resource": {
            "type": "news_ref",
            "data": {
                "api": {
                    "method": "GET",
                    "url": "http://s.xiaodu.baidu.com/v20161223/news/playlist?user_id=yinjie05_debug_monitor"
                }
            }
        },
        "views": {
            "type": "list",
            "list": [
                {
                    "title": "华谊兄弟的贺岁电影之路",
                    "summary": "最初的贺岁档从12月中下旬延伸至1月上旬，但由于众多等候上映的影片和庞大的观影消费需求，贺岁档的时间跨度也明显增长，如今在广义上一般认为从每年11月第三个周末起、至次年3月初的电影档期，都属于“贺岁档”。作为中国大陆最知名的综合性娱乐集团，1998年华谊兄弟正式进入影视界开发、制作及发行中国最受欢迎的影视作品，为中国贺岁电影档贡献了诸多口碑佳作，为观众们创造了一段段经典的银幕回忆。",
                    "image": "http://t12.baidu.com/it/u=2015004398,977977646&fm=170&s=CAD1458CDC9BB8D202F41DAF0300A040&w=218&h=146&img.PNG",
                    "url": "http://baijiahao.baidu.com/s?id=1559212650938821"
                },
                {
                    "title": "阿杜元宵节带病演唱 敬业精神令人称赞",
                    "summary": "有着独特沙哑嗓音的阿杜2月11日受邀，亮相九寨沟参加一年一度的元宵晚会。令人尤为感动的是，因演出地点海拔较高，阿杜遭遇高原反应，虽身体不舒服却强忍不适完成演出，其敬业精神令人夸赞。阿杜一连演唱3首广为流传的经典作品，让在场观众听得如痴如醉，出色的表演和真诚的演唱，让阿杜收获阵阵掌声。",
                    "image": "http://t10.baidu.com/it/u=2166724344,2688656461&fm=170&s=9A1A63847EC12AC4E8299114030070E0&w=218&h=146&img.JPEG",
                    "url": "http://music.yule.sohu.com/20170213/n480595253.shtml"
                },
                {
                    "title": "资讯 | 新片场CEO内部信：成立影业公司，《四平青年》将上院线",
                    "summary": "2016年是优质互联网影视作品的爆发年，越来越多正能量、高品质的网络电影出现，洗去了传统观众对网络影视内容的质疑，打开了网络电影建立健康积极生态的新气象。新片场“网络电影、网络剧出品发行”事业部踏入互联网影视行业不算早，但是在这一年的洗牌期中，他们依靠新片场旗下最大的创作人社区，形成了自有的人才库，从宣传发行入手，迅速占据市场，全年累计出品发行一百多部作品，影片整体播放量超过10亿次，与各视频平台保持紧密合作联系。",
                    "image": "http://t10.baidu.com/it/u=3140120850,105941560&fm=170&s=36F66936CDE1EF1140DC43E40300B03E&w=218&h=146&img.PNG",
                    "url": "http://baijiahao.baidu.com/s?id=1555002935513062"
                }
            ]
        }
    }
}
```


### directives 部分的说明

参考：[SpeechSynthesizer](../directives/SpeechSynthesizer.md) 语音播报（TTS）相关指令


### resource 部分的解释说明

存放新闻列表的地址。

```javascript
"resource": {
    "type": "news",
    "data": {
        "api": {
            "method": "GET",
            "url": "http://s.xiaodu.baidu.com/v20161223/news/playlist?user_id=yinjie05_debug_monitor"
        }
    }
},
```


## 获取新闻播放列表

新闻播放列表，默认返回10条新闻。

示例：http://s.xiaodu.baidu.com/v20161223/news/playlist?user_id=yinjie05_debug_monitor&page=1&page_size=10

参数：
- user_id: 用户id 
- page: 页码
- page_size: 每页请求新闻数量，默认为10

返回码：status为0表示成功，非0表示失败。

```javascript
{
    status: 0,
    code: null,
    data: [
        {
            "id": "3020804145379379001",
            "title": "华谊兄弟的贺岁电影之路",
            "summary": "最初的贺岁档从12月中下旬延伸至1月上旬，但由于众多等候上映的影片和庞大的观影消费需求，贺岁档的时间跨度也明显增长，如今在广义上一般认为从每年11月第三个周末起、至次年3月初的电影档期，都属于“贺岁档”。作为中国大陆最知名的综合性娱乐集团，1998年华谊兄弟正式进入影视界开发、制作及发行中国最受欢迎的影视作品，为中国贺岁电影档贡献了诸多口碑佳作，为观众们创造了一段段经典的银幕回忆。",
            "content_url": "http://s.xiaodu.baidu.com/v20161223/news/content?id=3020804145379379001",
            "url": "http://baijiahao.baidu.com/s?id=1559212650938821",
            "image": "",
            "thumb": "http://t12.baidu.com/it/u=2015004398,977977646&fm=170&s=CAD1458CDC9BB8D202F41DAF0300A040&w=218&h=146&img.PNG",
            "pubtime": "2017-02-13 18:17:40"
        },
        {
            "id": "10691447039517544028",
            "title": "阿杜元宵节带病演唱 敬业精神令人称赞",
            "summary": "有着独特沙哑嗓音的阿杜2月11日受邀，亮相九寨沟参加一年一度的元宵晚会。令人尤为感动的是，因演出地点海拔较高，阿杜遭遇高原反应，虽身体不舒服却强忍不适完成演出，其敬业精神令人夸赞。阿杜一连演唱3首广为流传的经典作品，让在场观众听得如痴如醉，出色的表演和真诚的演唱，让阿杜收获阵阵掌声。",
            "content_url": "http://s.xiaodu.baidu.com/v20161223/news/content?id=10691447039517544028",
            "url": "http://music.yule.sohu.com/20170213/n480595253.shtml",
            "image": "",
            "thumb": "http://t10.baidu.com/it/u=2166724344,2688656461&fm=170&s=9A1A63847EC12AC4E8299114030070E0&w=218&h=146&img.JPEG",
            "pubtime": "2017-02-13 18:01:50"
        },
        {
            "id": "2419829184223400427",
            "title": "资讯 | 新片场CEO内部信：成立影业公司，《四平青年》将上院线",
            "summary": "2016年是优质互联网影视作品的爆发年，越来越多正能量、高品质的网络电影出现，洗去了传统观众对网络影视内容的质疑，打开了网络电影建立健康积极生态的新气象。新片场“网络电影、网络剧出品发行”事业部踏入互联网影视行业不算早，但是在这一年的洗牌期中，他们依靠新片场旗下最大的创作人社区，形成了自有的人才库，从宣传发行入手，迅速占据市场，全年累计出品发行一百多部作品，影片整体播放量超过10亿次，与各视频平台保持紧密合作联系。",
            "content_url": "http://s.xiaodu.baidu.com/v20161223/news/content?id=2419829184223400427",
            "url": "http://baijiahao.baidu.com/s?id=1555002935513062",
            "image": "",
            "thumb": "http://t10.baidu.com/it/u=3140120850,105941560&fm=170&s=36F66936CDE1EF1140DC43E40300B03E&w=218&h=146&img.PNG",
            "pubtime": "2017-02-13 17:57:46"
        },
        {
            "id": "4067599035478312759",
            "title": "娱乐资本论获虎嗅年度最佳内容，我们会在内容这条路上死磕到底",
            "summary": "12月4日，2016年虎嗅F&amp;M创新节北京站开幕，娱乐资本论与三节课、腾讯研究院共同获颁年度内容合作机构。娱乐资本论2014年5月即入驻虎嗅，正如虎嗅F&amp;M创新节一贯秉持的真实犀利的态度，娱乐资本论也一直自诩为行业里的“匕首”“利剑”，自创立伊始就用独特视角与犀利言语的精心铺陈,为大众呈现多篇”另类爆款”。",
            "content_url": "http://s.xiaodu.baidu.com/v20161223/news/content?id=4067599035478312759",
            "url": "http://baijiahao.baidu.com/s?id=1552988326581526",
            "image": "",
            "thumb": "http://t10.baidu.com/it/u=705623784,4150857691&fm=170&s=BAB570840A679A515EC1628D0300C08A&w=218&h=146&img.PNG",
            "pubtime": "2017-02-13 17:56:08"
        },
        {
            "id": "4225000464409891217",
            "title": "资讯丨华谊兄弟收购英雄互娱暂告终止，双方合作仍将深化",
            "summary": "为了保护公司和广大投资者利益，公司董事会经审慎研究决定终止本次重大资产重组事项，并向深圳证券交易所申请公司股票复牌。重大资产重组指华谊兄弟拟以发行股份方式收购北京英雄互娱科技股份有限公司部分股份。尽管收购暂告终止，但双方合作的空间仍旧广阔。",
            "content_url": "http://s.xiaodu.baidu.com/v20161223/news/content?id=4225000464409891217",
            "url": "http://baijiahao.baidu.com/s?id=1552988313797763",
            "image": "",
            "thumb": "http://t11.baidu.com/it/u=2181793789,1064317744&fm=170&s=8A83934D3E415F53C4291D7C0300D03B&w=218&h=146&img.PNG",
            "pubtime": "2017-02-13 17:56:06"
        },
        {
            "id": "17797035842470588585",
            "title": "这才是爱情该有的模样《相亲》往期牵手情侣很甜蜜",
            "summary": "上期刚播出的节目中，台湾型男与女嘉宾圆圆的妹妹一见钟情，最终牵手，再度让网友发现了惊喜。许多网友表示，敢爱敢恨，坚持原则，这才是爱情该有的模样。此外，《中国式相亲》也首度公布了一些往期节目中牵手成功的男女嘉宾的近况，李博涵为宋京苹的喜好剃光头、张天舒决定去到廖晗辰的城市。牵手嘉宾幕后甜蜜很“虐狗”，网友直呼也想去相亲。",
            "content_url": "http://s.xiaodu.baidu.com/v20161223/news/content?id=17797035842470588585",
            "url": "http://ent.qq.com/a/20170213/034587.htm",
            "image": "",
            "thumb": "http://t10.baidu.com/it/u=2223215469,1221239100&fm=170&s=2BA6920B4C5B5AD4D21CFBFB03001087&w=218&h=146&img.JPEG",
            "pubtime": "2017-02-13 17:56:00"
        },
        {
            "id": "16623815886029134678",
            "title": "王全安执导马克思传记片 铁皮鼓男主主演",
            "summary": "知名导演王全安将执导传记题材影片《卡尔·马克思：最后的旅程》，德国资深演员马里奥·阿多夫将在片中饰演马克思一角。《卡尔·马克思：最后的旅程》讲述的是马克思晚年前往阿尔及尔的旅程，影片计划在2018年完成，2018年也恰好是马克思诞辰200周年。王全安曾凭借《图雅的婚事》摘得柏林电影节金熊奖，第67届柏林电影节已经揭幕，他也是本届柏林电影节的评委之一。",
            "content_url": "http://s.xiaodu.baidu.com/v20161223/news/content?id=16623815886029134678",
            "url": "http://ent.sina.com.cn/m/f/2017-02-13/doc-ifyamkzq1280447.shtml",
            "image": "",
            "thumb": "http://t11.baidu.com/it/u=1714899154,3099206762&fm=170&s=672223E7287326941C20ED3303001041&w=218&h=146&img.JPEG",
            "pubtime": "2017-02-13 17:18:00"
        },
        {
            "id": "10236257163723268449",
            "title": "陈凯歌一家拍全家福 儿子帅气妻子优雅",
            "summary": "2月12日，陈凯歌一家全家福曝光，照片中，陈凯歌搂着儿子，妻子陈红坐在凳子上，端庄优雅。儿子陈飞宇阳光帅气。整个照片采用工笔画风，衬得全家气质出众。据悉，这张全家福是陈凯歌一家录制真人秀《熟悉的味道》的官方海报，低调的陈凯歌陈红夫妇首次带小儿子一起亮相真人秀节目，引发众人关注。",
            "content_url": "http://s.xiaodu.baidu.com/v20161223/news/content?id=10236257163723268449",
            "url": "http://yule.sohu.com/20170213/n480589157.shtml",
            "image": "",
            "thumb": "http://t12.baidu.com/it/u=2267541656,2721306228&fm=170&s=6AA0CC4DD843EB5F4A20B0A503007043&w=218&h=146&img.JPEG",
            "pubtime": "2017-02-13 17:17:31"
        },
        {
            "id": "16384386512894460596",
            "title": "钱是大问题！《魔兽》导演期待拍《魔兽2》",
            "summary": "近日，《魔兽》大电影的导演邓肯·琼斯在和粉丝互动时表示仍想要拍摄《魔兽》电影续集。摆在他面前的一个现实问题是虽然《魔兽》电影在中国市场揽获了2.21 亿美元，但是影片的全球票房也只达到了4.3 亿美元。显而易见，邓肯·琼斯如果想要拍摄《魔兽》续集的话，必须要考虑传奇影业会不会投资。这对于琼斯来说无疑是个严肃的问题。",
            "content_url": "http://s.xiaodu.baidu.com/v20161223/news/content?id=16384386512894460596",
            "url": "http://comic.sina.com.cn/fanyule/2017-02-13/doc-ifyamkzq1280358.shtml",
            "image": "",
            "thumb": "http://t11.baidu.com/it/u=1038732181,3723676747&fm=170&s=171451CE465B3DD451F1988003009081&w=218&h=146&img.JPEG",
            "pubtime": "2017-02-13 17:16:11"
        },
        {
            "id": "17415159588394100071",
            "title": "黄晓明节目现场被曝发烧中 “劳模”是拼出来的",
            "summary": "昨晚播出的某综艺节目，黄晓明在猜评团中“神探”上身，对于各MC邀请的神秘嘉宾好友几乎每猜必中。猜评团成员张大大突然现场爆料黄晓明不仅正在发烧中，还知道他前两周去做正骨，痛到大叫，令黄爸爸凌晨两点在隔壁房间听到儿子的叫声十分心疼。“劳模”背后的努力和坚持令人敬佩。",
            "content_url": "http://s.xiaodu.baidu.com/v20161223/news/content?id=17415159588394100071",
            "url": "http://ent.qq.com/a/20170213/033442.htm",
            "image": "",
            "thumb": "http://t11.baidu.com/it/u=258863470,208703076&fm=170&s=CBD4D1AE0937A5EF5EB9458603003007&w=218&h=146&img.JPEG",
            "pubtime": "2017-02-13 17:16:00"
        }
    ],
    message: null
}

```


## 获取新闻内容接口

新闻内容包含图片和问题，通过type字段区分。

示例：http://s.xiaodu.baidu.com/v20161223/news/content?id=17415159588394100071

参数：id, 新闻id

返回码：status为0表示成功，非0表示失败。

```
{
    status: 0,
    code: null,
    data: [
        {
            type: "image",
            data: {
                big: {
                    height: 680,
                    url: "http://t11.baidu.com/it/u=2235963898,1792389728&fm=170&s=CBD4D1AE0937A5EF5EB9458603003007&w=623&h=680&img.JPEG",
                    width: 623
                },
                original: {
                    height: 680,
                    url: "http://img1.gtimg.com/ent/pics/hv1/217/233/2185/142139257.jpg",
                    width: 623
                },
                original_third: {
                    height: 680,
                    url: "http://img1.gtimg.com/ent/pics/hv1/217/233/2185/142139257.jpg",
                    width: 623
                },
                small: {
                    height: 360,
                    url: "http://t11.baidu.com/it/u=279339871,159264062&fm=170&s=CBD4D1AE0937A5EF5EB9458603003007&w=480&h=360&img.JPEG",
                    width: 480
                }
            }
        },
        {
            type: "text",
            data: "节目录制现场"
        },
        {
            type: "image",
            data: {
                big: {
                    height: 302,
                    url: "http://t11.baidu.com/it/u=2144948446,1705532450&fm=170&s=928048A70E7A72964D19900203001011&w=479&h=302&img.JPEG",
                    width: 479
                },
                original: {
                    height: 302,
                    url: "http://img1.gtimg.com/ent/pics/hv1/222/233/2185/142139262.jpg",
                    width: 479
                },
                original_third: {
                    height: 302,
                    url: "http://img1.gtimg.com/ent/pics/hv1/222/233/2185/142139262.jpg",
                    width: 479
                },
                small: {
                    height: 302,
                    url: "http://t11.baidu.com/it/u=188324419,72406784&fm=170&s=928048A70E7A72964D19900203001011&w=479&h=302&img.JPEG",
                    width: 479
                }
            }
        },
        {
            type: "text",
            data: "黄晓明拍戏受伤"
        },
        {
            type: "image",
            data: {
                big: {
                    height: 680,
                    url: "http://t11.baidu.com/it/u=2176538020,1732823474&fm=170&s=3EE2C704CA23529C260C09B2030080C3&w=509&h=680&img.JPEG",
                    width: 509
                },
                original: {
                    height: 680,
                    url: "http://img1.gtimg.com/ent/pics/hv1/233/233/2185/142139273.jpg",
                    width: 509
                },
                original_third: {
                    height: 680,
                    url: "http://img1.gtimg.com/ent/pics/hv1/233/233/2185/142139273.jpg",
                    width: 509
                },
                small: {
                    height: 360,
                    url: "http://t11.baidu.com/it/u=219913993,99697808&fm=170&s=3EE2C704CA23529C260C09B2030080C3&w=480&h=360&img.JPEG",
                    width: 480
                }
            }
        },
        {
            type: "text",
            data: "黄晓明写真"
        },
        {
            type: "text",
            data: "腾讯娱乐讯昨晚（2月12日）播出的某综艺节目，黄晓明在猜评团中“神探”上身，对于各MC邀请的神秘嘉宾好友几乎每猜必中。"
        },
        {
            type: "text",
            data: "大部分都不是歌手出身的MC们，为了在这次歌会中有精彩的表现，也是极尽突破挑战自我。猜评团成员张大大突然现场爆料黄晓明不仅正在发烧中，还知道他前两周去做正骨，痛到大叫，令黄爸爸凌晨两点在隔壁房间听到儿子的叫声十分心疼。"
        },
        {
            type: "text",
            data: "黄晓明出道近二十年，拍戏一向拼命的他，虽然不是专业动作演员，拍动作戏也尽量亲身上阵，所以多年来身上的大伤小伤一直不断，而为了不影响剧组的进度，常常都是不顾医生的“工作禁令”就回到剧组继续工作。"
        },
        {
            type: "text",
            data: "2003年拍摄《龙票》时在沙漠翻车导致颈椎严重骨折，医生就勒令让黄晓明休息几个月，黄晓明担心剧组工作人员都在等他，坚持继续拍戏，医生说“你疯了吗，如果不好好休息就会瘫痪！”但他仍旧坚持开工，于是，就此留下了严重的后遗症。直到现在，黄晓明都无法睡正常的枕头，必须要特制的圆形枕头睡觉，他的颈椎才不会那么疼。他还曾自曝其实有“威亚恐惧症”，几年前拍摄一部电影时，从威亚上直接掉了下来，脚趾粉碎性骨折，打了4根钢钉，2根钢针。但他在伤后40天还是坚持去拍戏，打着绷带吊着腿继续吊威亚。“劳模”背后的努力和坚持令人敬佩。"
        }
    ],
    message: null
}
```
