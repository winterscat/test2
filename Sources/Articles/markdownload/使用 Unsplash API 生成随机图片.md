---
url: https://www.imyangyong.com/blog/2020/06/javascript/%E4%BD%BF%E7%94%A8%20Unsplash%20API%20%E7%94%9F%E6%88%90%E9%9A%8F%E6%9C%BA%E5%9B%BE%E7%89%87/
date: 2022-08-12 21:44:21
tag: 
summary: JavaScript Cooooder.ð
---
## [](#Unsplash "Unsplash")Unsplash

å¦æä½ æ³ä½¿ç¨åè´¹çæçå¾çæ¶ï¼æ è®ºä½ æ¯å¦ç¨äºåä¸ç¨éï¼[Unsplash](https://unsplash.com/) æ¯ä¸éçéæ©ã

æèªå·±ä¹ç»å¸¸ç¨å®æ¥å¶ä½å¤§åèæ¯å¾çï¼ä¾å¦ï¼[https://www.imyangyong.com](https://www.imyangyong.com/) ã

è½ç¶ä»ä»¬ä¸ºå¼åäººåæä¾äºå¾æ£ç APIï¼ä½ä»ä»¬ä¹æä¾äºéè¿ URL è®¿é®éæºå¾ççéé¡¹ã

## [](#1-é»è®¤éæº "1. é»è®¤éæº")1. é»è®¤éæº

è¯·çè¿ä¸ªä¾å­ï¼ä»ä»ä»¬å·¨å¤§çå­å¨ä¸­çæéæºçå¾çã

<table><tbody><tr><td><pre><span>1</span><br></pre></td><td><pre><span>https://source.unsplash.com/random</span><br></pre></td></tr></tbody></table>

## [](#æå®ç¨æ· "æå®ç¨æ·")æå®ç¨æ·

æä»¬è¿å¯ä»¥ä»ç¹å®ç¨æ·è´¦å·ä¸­çæéæºå¾åãURL æ ¼å¼æ¯è¿æ ·ç:

<table><tbody><tr><td><pre><span>1</span><br></pre></td><td><pre><span>https://source.unsplash.com/user/{USERNAME}</span><br></pre></td></tr></tbody></table>

ä½ å¯ä»¥å°è¯åå»ä¸é¢çé¾æ¥ï¼ä»æçè´¦å·ä¸­éæºçæå¾çï¼

[https://source.unsplash.com/user/angusyang9/likes](https://source.unsplash.com/user/angusyang9/likes)

## [](#3-æå®å°ºå¯¸ "3. æå®å°ºå¯¸")3. æå®å°ºå¯¸

è¿æä¸ä¸ªéé¡¹å¯ä»¥è®¾ç½®è¦çæçå¾åçå¤§å°ãåè¿æ ·:

<table><tbody><tr><td><pre><span>1</span><br></pre></td><td><pre><span>https://source.unsplash.com/random/{WIDTH}x{HEIGHT}</span><br></pre></td></tr></tbody></table>

è®©æä»¬çæä¸ 300 x 300 å¤§å°çå¾çï¼

[https://source.unsplash.com/random/300Ã300](https://source.unsplash.com/random/300%C3%97300)

## [](#4-ä¾æ®å³é®è¯æç´¢ "4. ä¾æ®å³é®è¯æç´¢")4. ä¾æ®å³é®è¯æç´¢

è¿ä¸ªççå¾æ£ãä½ å¯ä»¥ä»æç´¢è¯çæå¾åãè®©æä»¬æç´¢ä¸åå¸åå¤æï¼éå¸¸æåæï¼ï¼

[https://source.unsplash.com/random/?city,night](https://source.unsplash.com/random/?city,night)

å½ç¶ï¼ä½ å¯ä»¥ä¸å°ºå¯¸éåä½¿ç¨ï¼

[https://source.unsplash.com/random/900Ã700/?fruit](https://source.unsplash.com/random/900%C3%97700/?fruit)

## [](#ä»£ç ç¤ºä¾ "ä»£ç ç¤ºä¾")ä»£ç ç¤ºä¾

ä»¥ä¸æ¯ react ä¸­çä»£ç çæ®µï¼

<table><tbody><tr><td><pre><span>1</span><br><span>2</span><br><span>3</span><br><span>4</span><br><span>5</span><br><span>6</span><br><span>7</span><br><span>8</span><br><span>9</span><br><span>10</span><br><span>11</span><br><span>12</span><br><span>13</span><br><span>14</span><br><span>15</span><br><span>16</span><br><span>17</span><br><span>18</span><br><span>19</span><br><span>20</span><br><span>21</span><br><span>22</span><br><span>23</span><br><span>24</span><br><span>25</span><br><span>26</span><br><span>27</span><br><span>28</span><br><span>29</span><br><span>30</span><br><span>31</span><br><span>32</span><br></pre></td><td><pre><span><span><span>class</span> <span>RandomImg</span> <span>extends</span> <span>React</span>.<span>Component</span> </span>{</span><br><span>  <span>constructor</span>() {</span><br><span>    <span>super</span>();</span><br><span>    <span>this</span>.state = {</span><br><span>      bgImageUrl: <span>require</span>(<span>'./default.jpeg'</span>)</span><br><span>    }</span><br><span>  }</span><br><span>  </span><br><span>  componentDidMount() {</span><br><span>    <span>this</span>.generateImage();</span><br><span>  }</span><br><span>  </span><br><span>  generateImage(){</span><br><span>    fetch(<span>`https://source.unsplash.com/random/?people`</span>).then(<span>(<span>response</span>) =&gt;</span> {</span><br><span>      preloadImage(response.url);</span><br><span>    })</span><br><span>	}</span><br><span>  </span><br><span>  preloadImage(url) {</span><br><span>    <span>let</span> img = <span>new</span> Image();</span><br><span>    img.src = url;</span><br><span>    img.onload = <span><span>()</span> =&gt;</span> {</span><br><span>      <span>this</span>.setState({</span><br><span>        bgImageUrl: url</span><br><span>      });</span><br><span>    }</span><br><span>	}</span><br><span>  </span><br><span>  render() {</span><br><span>    <span>return</span> <span><span>&lt;<span>img</span> <span>src</span>=<span>{bgImageUrl}</span> /&gt;</span></span></span><br><span>  }</span><br><span>}</span><br></pre></td></tr></tbody></table>

## [](#åèé¾æ¥ "åèé¾æ¥")åèé¾æ¥

*   [Generate Random Images From Unsplash Without Using The API](https://awik.io/generate-random-images-unsplash-without-using-api/)