# ðæºè½åä½å¹³å°ä½¿ç¨æ¹æ³

æ³¨ï¼è¯·åå°æ¨¡åæä»¶ä¸è½½è³ `Back-end/mysite/data/` ç®å½ã<br>é¾æ¥ï¼https://pan.baidu.com/s/1hBVIp5RNkvVeyS8TVufEaQ  æåç ï¼asdf

## ð åç½®éæ±

- Node.js >= 12.0.0

- Yarn

- æéè¦çPythonåï¼è§back-end/mysite/requirements.txt)

  - ```shell
    pip install -r requirements.txt
    ```

## ð å®è£

### ðåç«¯

```shell
cd Front-end
yarn install
yarn start
```

ç°å¨ä½ å¯ä»¥å¨æµè§å¨ä¸­è®¿é® <http://localhost:3000/>

![](./imgs/interface.png)

### ðåç«¯

```shell
cd Back-end/mysite
python manage.py runserver
```

**å¨summary/utliä¸­å­æ¾æè¦çæç¸å³ä»£ç åæ¨¡åå¨summaryæä»¶å¤¹ä¸çè§å¾å±view.pyç¸å³ä½ç½®è°ç¨çæå½æ°**

## ðåè½ç®ä»

### èªå¨æ é¢çæ

#### é¡¹ç®æè¿°

æ ¹æ®æç« åå®¹çææç« æ é¢

#### ç¯å¢éç½®

Python çæ¬ï¼3.8
PyTorch çæ¬ï¼1.10.0
CUDA çæ¬ï¼11.3

æéç¯å¢å¨ `requirements.txt` ä¸­å®ä¹ã

#### æ°æ®

* è½¯ä»¶æ¯å®æ¹æ°æ® http://www.cnsoftbei.com/plus/view.php?aid=729
* å¼æºæè¦æ°æ® https://zhuanlan.zhihu.com/p/341398288

#### ç®å½ç»æ

```
./
âââ README.md
âââ requirements.txt        # Pythonåä¾èµæä»¶ 
âââ check/                  # ä¿å­æ¨¡å
âââ logs/                   # ä¿å­tfeventæä»¶
âââ data/                   # ä¿å­è®­ç»æ°æ®
â   âââ train.json
â   âââ dev.json
â   âââ ...
âââ vocab/                  # è¯è¡¨ç®å½
â   âââ vovab.txt      # ç¨äºæå»ºtokenizerçè¯è¡¨
âââ config/   
â   âââ config.json         # æ¨¡åéç½®
âââ src/                    # æ ¸å¿ä»£ç 
â   âââ config.py      # æ¨¡åãè®­ç»åæ°
â   âââ dataset.py     # æ°æ®é
â   âââ finetune.py    # å¾®è°
â   âââ generate.py    # æµè¯çæ
â   âââ model.py       # æ¨¡åå®ä¹
â   âââ train.py       # è®­ç»
â   âââ utils.py       # å·¥å·å½æ°
```

```
æ³¨ï¼vocab.txtæ¥èª https://huggingface.co/hfl/chinese-macbert-base/blob/main/vocab.txt
```

#### æ¨¡å

* GPT2
  ![](./imgs/model.png)

```
    æ³¨ï¼
    1. NãMåå«ä¸ºåå®¹åæ é¢çæå¤§é¿åº¦ãè¥è¶è¿æå¤§é¿åº¦ï¼æ é¢ç´æ¥ææå¤§é¿åº¦æªæ­ï¼åå®¹ååå«æªåæå¤§é¿åº¦ä¸åçå¼å¤´åç»å°¾ã  
    2. [Conetent] å [Title] ä¸ºæ·»å çç¹æ®å­ç¬¦ï¼ç¨äºåºååå®¹åæ é¢çæ®µã
```

* Loss
  ![](./imgs/loss.png)

#### çææµè¯

![](./imgs/test.png)

#### è¿è¡æµç¨

```shell
è®­ç» -> å¾®è° -> æµè¯
```

```shell
pip install -r requirements.txt
python src/train.py
python src/finetune.py
python src/generate.py 
```

### èªå¨æè¦çæ

#### éè¦çèµæºä¸è½½

ç±äºä½¿ç¨çè¯åéè¡¨ç¤ºåè®­ç»æ°æ®éè¿å¤§ï¼å¹¶æ²¡æä½ä¸ºæäº¤æä»¶çä¸é¨åæäº¤ï¼æå¦éå¨æ¬å°è¿è¡é¨ç½²ï¼è¯·å®æå¦ä¸èµæºçä¸è½½ï¼

+ åºäºå¾®åè¯­æåºè®­ç»ç$300$ç»´è¯åé
+ NLPCC2017æè¦æ°æ®

#### ä¸è½½

* åºäºå¾®åè¯­æåºè®­ç»ç$300$ç»´è¯åé$300$ç»´è¯åéï¼æ¥æºäºhttps://github.com/Embedding/Chinese-Word-Vectors
  * ä¸ºå å¿«ä¸è½½ï¼è¯·ä»[æ­¤å¤](http://image-hosting-404.oss-cn-beijing.aliyuncs.com/source/sgns.weibo.word.zip)ä¸è½½ã
* `NLPCC2017`æè¦æ°æ®ï¼æ¥æºäºhttps://github.com/liucongg/GPT2-NewsTitle
  * ä¸ºå å¿«ä¸è½½ï¼è¯·ä»[æ­¤å¤](http://image-hosting-404.oss-cn-beijing.aliyuncs.com/source/nlpcc_data.json)ä¸è½½ã

ä¸è½½å®æå°å¦ä¸èµæºæ¾å¨ç®å½`backend/textrank/data`ä¸­å³å¯

- [x] textRankè®¡ç®å³é®è¯
- [x] textRankè®¡ç®å³é®å¥
- [x] webåç«¯HTMLçé¢
- [x] Djangoåç«¯
- [x] transformer

- [x] æ£æ¥ä¸ä¸ªè¯å¨åç¨è¯è¡¨ä¸­ ç¨å­å¸æ ä¼å
- [x] è®¡ç®å³é®å¥ä¸­ ç¨å­å¸æ ä¼å
- [x] æ´ç»ç²åº¦çåå¥
- [x] textrankå¯ä»¥è¿ä¸æ­¥æ¹è¿ï¼å¦å å¥å¥å­é¿åº¦çæ©ç½ï¼æèä½¿ç¨å¥åéå¤æ­ç¸ä¼¼æ§


#### åèèµææ¥æº

* åç¨è¯è¡¨æ¥æºï¼https://github.com/goto456/stopwords
* æ¸åæ°æ®éæ¥æºï¼http://thuctc.thunlp.org/
* æ¸åæ°é»æ°æ®éæ¥æºï¼https://thunlp.oss-cn-qingdao.aliyuncs.com/THUCNews.zip



