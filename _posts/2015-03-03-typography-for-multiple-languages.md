---
layout: post
title: 복수 언어 사용 시의 타이포그래피
date: 2016-01-03 11:41:00
lang: ko
comments: true
---

<style type='text/css' scoped>
.figure {
  font-size: 12px;
  line-height: 1.5;
  width: 400px;
  border: 1px solid #e8e8e8;
  padding: 12px;
}
.figure > li {
  list-style-type: none;
}
.figure > li:not(:last-child) {
  padding-bottom: 12px;
}
</style>

블로그에 한국어로도 영어로도 글을 올리려다 보니 스타일 지정에 있어 까다로운 문제들을 발견했습니다.

우선 문자에 따라 글꼴 크기, 줄간, 행간등이 달라야 함을 깨달았습니다. 예를 들면 한글의 경우에는 보통 줄간을 2.0 가까이 넓게 주는 반면 영문의 경우에는 보통 줄간을 1.5 혹은 그 이하로 좁게 주는 편입니다. 이는 상용 한글 글꼴이 꽉 찬 네모꼴이기에 같은 글꼴 크기에서 줄과 줄 사이의 공간이 훨씬 적게 나타나기에 생기는 것입니다.

<div class='figure'>
  <li style="font-family:'Nanum Myeongjo'; line-height: 2.0;">
    청춘의 아니더면, 희망의 것이다. 보라, 수 찬미를 곧 그들의 있으랴? 것은 그들은 소금이라 우리 사라지지 하는 위하여서. 이것을 같은 이상의 산야에 구하지 싸인 부패뿐이다. 그들의 동력은 그러므로 봄바람이다. 철환하였는가 뜨고, 같은 만천하의 착목한는 위하여서, 인생을 따뜻한 그리하였는가?
  </li>
  <li style="font-family:'Georgia'; line-height: 1.5;">
    Lorem ipsum dolor sit amet, eu nam enim recusabo, at usu eligendi oportere assentior. Ex iudico quodsi audiam eam. Enim vivendum an eum, quis esse facilisis ex nec. Mel ut consul meliore. Ut elit ornatus vix. Nam inani aperiam et. Qui at enim saepe interpretaris, nec ad alia postea aliquam, eos cu tollit melius ocurreret.
  </li>
</div>
<figcaption>예시 1. 위는 나눔명조 줄간 2.0, 아래는 Georgia 줄간 1.5.</figcaption>

문자에 따라 사용하는 영문 글꼴이 달라야 할 수도 있음을 깨달았습니다. 예를 들면 한글 글꼴로 나눔명조를 사용한다고 해 봅시다. 나눔명조에서 기본으로 삼고 있는 영문 글꼴은 선이 매우 얇아 나눔명조와 함께 사용되기에는 적합하지만 영문 전용 글에 사용되기에는 너무 얇은 느낌이 있습니다.

<div class='figure'>
  <li style="font-family:'Nanum Myeongjo';">
    Lorem ipsum dolor sit amet, eu nam enim recusabo, at usu eligendi oportere assentior. Ex iudico quodsi audiam eam. Enim vivendum an eum, quis esse facilisis ex nec. Mel ut consul meliore. Ut elit ornatus vix. Nam inani aperiam et. Qui at enim saepe interpretaris, nec ad alia postea aliquam, eos cu tollit melius ocurreret.
  </li>
  <li style="font-family:'Georgia';">
    Lorem ipsum dolor sit amet, eu nam enim recusabo, at usu eligendi oportere assentior. Ex iudico quodsi audiam eam. Enim vivendum an eum, quis esse facilisis ex nec. Mel ut consul meliore. Ut elit ornatus vix. Nam inani aperiam et. Qui at enim saepe interpretaris, nec ad alia postea aliquam, eos cu tollit melius ocurreret.
  </li>
</div>
<figcaption>예시 2. 위는 나눔명조, 아래는 Georgia. 각각 줄간 1.5.</figcaption>

보통 영문 글꼴과 한글 글꼴을 따로 사용하기 위한 방법으로 `font-family` 속성에 영문과 한글을 차례대로 나열하는 방법이 있습니다. 이렇게 하면 영문의 경우 제일 먼저 선언된 영문 글꼴을 사용하게 되고 한글의 경우 영문 글꼴에 해당 문자가 없음을 확인한 후 그 다음 선언된 한글 글꼴을 사용하게 됩니다. 하지만 이렇게 하면 두 글꼴 병기되었을 때 조화가 잘 이루어지도록 글꼴을 세심하게 선택해야 하는 문제가 있습니다. 아래 예시 3를 보면 위의 경우 아래보다 문장 부호, 숫자, 영문에 있어서 글의 결이 확실히 도드라지게 튀어 보이는 문제가 있음을 확인할 수 있습니다.

<div class='figure' style='line-height:2.0;'>
<li style="font-family:Georgia, 'Nanum Myeongjo';">
  청춘의 아니더면, 희망의 것이다 (Lorem ipsum dolor sit). 보라, 3,650 수 찬미를 곧 그들의 있으랴? 그들의 동력은 그러므로 봄바람이다. ABC 철환하였는가 뜨고, 같은 만천하의 착목한는 위하여서 (Ut elit ornatus vix), 인생을 따뜻한 그리하였는가?
</li>
<li style="font-family:'Nanum Myeongjo';">
  청춘의 아니더면, 희망의 것이다 (Lorem ipsum dolor sit). 보라, 3,650 수 찬미를 곧 그들의 있으랴? 그들의 동력은 그러므로 봄바람이다. ABC 철환하였는가 뜨고, 같은 만천하의 착목한는 위하여서 (Ut elit ornatus vix), 인생을 따뜻한 그리하였는가?
</li>
</div>
<figcaption>예시 3. 위는 <code>font-family:Georgia,'Nanum Myeongjo'</code>. 아래는 <code>font-family:Georgia</code>.</figcaption>

저는 html 태그에 lang 설정을 준 후 scss 파일에서 다음과 같은 식으로 언어에 따라 다른 설정을 주는 방법으로 이 문제를 해결하였습니다. mixin을 적절하게 사용하여 이를 더 간단하게 해결할 방법도 있을 것 같은데 아직 좋은 방법을 찾진 못했습니다. 수직 그리드라인에 맞춰서 디자인을 짜려다 보니 스타일 파일이 많이 복잡해져서, 이러느니 그냥 영문 블로그 한글 블로그를 따로 운영하는 게 좋지 않을까 하는 생각도 들더군요.

{% highlight scss %}
body {
  &:lang(ko) {
    font-family: $font-family-ko;
    line-height: $line-height-ko;
  }
  &:lang(en) {
    font-family: $font-family-en;    
    line-height: $line-height-en;
  }      
}
{% endhighlight %}
