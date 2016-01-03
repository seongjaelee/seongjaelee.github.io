---
layout: post
title: Bordered tables preserving vertical rhythm
date: 2016-01-03
lang: en
comments: true
---

<style type='text/css' scoped>
.figure {
  margin-left: 12px;
  float: right;
}
.figure-wrapper {
  padding: 12px;
  border: 1px solid black;
  background-color: white;
}
.gridline {
  background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='2' height='20'><rect x='0' y='19' width='1' height='1' fill='red'></rect></svg>");
}
.figure tr {
  background-image: none;
}
.figure table, .figure tr, .figure td {
  padding: 0;
  margin: 0;
  border: 0;
}
.figure td {
  font-size: 12px;
  line-height: 20px;
}
#figure1 td {
  border-bottom: 1px solid rgba(0, 0, 255, 0.4);
}
#figure2 td {
  padding-top: 10px;
  padding-bottom: 9px;
  border-bottom: 1px solid rgba(0, 0, 255, 0.4);
}
#figure3 td {
  background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1' height='20'><rect x='0' y='19' width='1' height='1' fill='blue' fill-opacity='0.4'></rect></svg>");
  background-repeat: repeat-x;
  background-position: bottom;
}
</style>

The height of a table row is defined by the the sum of vertical borders, paddings, margins, and line height multiplied by the number of lines. If we want to add a vertical border of 1px, while keeping the line-height of the text to be grid size, the height of the row is off by 1px. In this article, I present all my past trials and show the solution using background-image property.

From now on, I will use the following table example for all figures.

{% highlight html %}
<table>
  <tr><td>Hello World</td></tr>
  <tr><td>Hello World</td></tr>
  <tr><td>Hello World<br>Hello World</td></tr>
</table>
{% endhighlight %}
{% highlight css %}
td {
  font-size: 12px;
  line-height: 20px;
}
{% endhighlight %}

<div class='figure' id='figure1'>
  <div class='figure-wrapper'>
    <div class='gridline'>
      <table>
        <tr><td>Hello World</td></tr>
        <tr><td>Hello World<br>Hello World</td></tr>
        <tr><td>Hello World</td></tr>
      </table>
    </div>
  </div>
  <figcaption>Figure 1.</figcaption>
</div>

Figure 1 is the naïve use of the table just adding 1px border on the bottom. Here, gridlines are rendered as red dots (24px), while table row borders are rendered as blue lines. We can see the discrepency adds up as we have more rows.

{% highlight css %}
td {
  border-bottom: 1px solid rgba(0, 0, 255, 0.4);
}
{% endhighlight %}

<div class='figure' id='figure2'>
  <div class='figure-wrapper'>
    <div class='gridline'>
      <table>
        <tr><td>Hello World</td></tr>
        <tr><td>Hello World<br>Hello World</td></tr>
        <tr><td>Hello World</td></tr>
      </table>
    </div>
  </div>
  <figcaption>Figure 2.</figcaption>
</div>

Another alternative is to make the sum of vertical padding and border to be the multiplication of the baseline grid. It surely works, but it will take much more vertical spaces.


{% highlight css %}
tr {
  padding-top: 10px;
  padding-bottom: 9px;
  border-bottom: 1px solid rgba(0, 0, 255, 0.4);
}
{% endhighlight %}


<div class='figure' id='figure3'>
  <div class='figure-wrapper'>
    <div class='gridline'>
      <table>
        <tr><td>Hello World</td></tr>
        <tr><td>Hello World<br>Hello World</td></tr>
        <tr><td>Hello World</td></tr>
      </table>
    </div>
  </div>
  <figcaption>Figure 3.</figcaption>
</div>

All these solutions were unsatisfactory, so I had been avoiding the use of bordered tables, until I found this solution using background-image property.

{% highlight css %}
tr {
  background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1' height='20'><rect x='0' y='19' width='1' height='1' fill='blue' fill-opacity='0.4'></rect></svg>");
  background-repeat: repeat-x;
  background-position: bottom;
}
{% endhighlight %}
