---
layout: post
title:  유니버설 디자인 서체, KoddiUD 온고딕
date:   2024-10-29 07:33:00
lang:   ko
comments: true
---

2020년, 닌텐도 스위치를 사용하다가 펌웨어에서 사용하는 기본 한글 서체가 눈에 띄였습니다. 레트로 감성과 정갈함이 조화롭게 어우러진 그 서체는 바로 [모리사와의 "UD신고 한글"][morisawa]이었죠. UD는 유니버설 디자인 (Universal Design)의 약자로, 문자의 모양을 판별하기 쉽게 하여 저시력자나 고령자도 문자를 쉽게 인지하고 비슷한 모양의 다른 문자들과의 구분성을 높여 오독의 가능성을 낮추는 것을 주 목표로 디자인된 서체라는 의미입니다. 당시 모라사와 홈페이지에서 유니버설 디자인 서체에 대한 정보를 접하며 그 개념에 깊이 공감하게 되었습니다. 모리사와의 "UD신고" 서체는 오픈라이선스가 아니라 아쉬움을 뒤로 하고 포기했지만, 모리사와 홈페이지의 그 정갈한 레이아웃은 항상 기억에 남아 그 이후에도 종종 방문하여 감탄하곤 했습니다.

사실 문자와의 구분성을 높여 오독의 가능성을 낮추는 서체 디자인은 유니버설 디자인에 국한되지 않고 이미 널리 사용되고 있습니다. 예를 들면 코딩을 위한 서체는 숫자 0과 영어 대문자 O, 숫자 1과 영어 소문자 l, 영어 대문자 I를 명확히 구분되게 하는 등의 문자 판독성(legibility)을 극대화 하는 디자인을 택하는 경우가 많습니다. 또한, 2021년 트위터에서는 계정명에 이러한 유사한 문자를 사용하여 유명 계정을 사칭하는 문제를 해결하기 위해 유사한 문자들을 확연히 구분되게 강조하는 디자인의 Twitter Chirp 서체를 계정명에만 적용하여 화제가 되기도 했죠.[^1][^2]

그러던 중 2024년, 우연히 윤디자인그룹과 한국장애인개발원이 함께 개발한 KoddiUD 온고딕 서체를 접하게 되었습니다. 2021년 장애인의날을 맞아 오픈라이선스로 배포된 이 서체인데요, "고령자, 노안, 저시력자 등 시력 약자들도 인지하기 쉽도록 만들어진 글꼴"로 "개발과정에서 시각장애인 30명을 포함한 10~70대 332명을 대상으로 타 고딕 글꼴과 함께 사용성 평가를 진행하여 판독성, 가독성의 우수함을 검증받"았다고 밝혔습니다.[^3] 글자 사이사이의 여백에 신경을 써 작은 글씨에서도 읽기 좋게 만든 것이 확실히 느껴지더군요. 그래서 제 깃허브 페이지에도 이를 적용하기로 하였습니다. 아름답기도 하지만, 모바일의 작은 화면에서도 제 글이 신문을 읽는 것처럼 편안히 읽히길 바랬으니까요. 저는 요즈음 전자책에도 이 서체를 적용해서 보고 있답니다.

KoddiUD 온고딕 서체에 대해 더 알고 싶으시다면 다음 링크를 참고하세요.
- 윤디자인 - 한국장애인개발원 KoddiUD 온고딕: [https://yoondesign.com/koddiud/](https://yoondesign.com/koddiud/)
- 한국장애인연구원 - 유니버설디자인 서체: [https://www.koddi.or.kr/ud/sub1_2](https://www.koddi.or.kr/ud/sub1_2)

웹사이트에서 KoddiUD 온고딕을 적용하고 싶다면, 무료 한글 서체를 널리 공유하는 눈누에서 운영하는 CDN을 사용하는 것을 추천합니다. CSS에 다음 구문을 집어넣으시면 됩니다.
{% highlight css %}
@font-face {
    font-family: 'KoddiUDOnGothic-Regular';
    src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/noonfonts_2105_2@1.0/KoddiUDOnGothic-Regular.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}
{% endhighlight %}
가장 최신 지원 코드는 [눈누의 KoddiUD 온고딕 페이지][noonnu]에서 확인할 수 있습니다.

[morisawa]: https://www.morisawa.co.kr/fonts/ud-fonts
[noonnu]: https://noonnu.cc/en/font_page/674
[^1]: [https://www.gq.com/story/twitter-chirp-new-typeface](https://www.gq.com/story/twitter-chirp-new-typeface)
[^2]: [https://mashable.com/article/twitter-new-font-fights-impersonators](https://mashable.com/article/twitter-new-font-fights-impersonators)
[^3]: [https://www.koddi.or.kr/ud/sub1_2](https://www.koddi.or.kr/ud/sub1_2)
