---
layout: post
title: Bordered tables preserving vertical rhythm
date: 2016-01-03
lang: en
comments: true
---

<style type='text/css' scoped>
.figure-wrapper {
  padding: 12px;
  border: 1px solid #e8e8e8;
  background-color: white;
}
.gridline {
  background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='2' height='20'><rect x='0' y='19' width='1' height='1' fill='red'></rect></svg>");
}
.figure-wrapper tr {
  background-image: none;
}
.figure-wrapper table, .figure-wrapper tr, .figure-wrapper td {
  padding: 0;
  margin: 0;
  border: 0;
}
.figure-wrapper td {
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

The height of a table row is defined by the the sum of vertical borders, paddings, margins, and line height multiplied by the number of lines. Adding a vertical border of 1px height makes the row to be off by 1px from the grid, breaking the vertical rhythm. In this article, I present my year-long journey to create a pixel-perfect bordered table and show the ultimate solution using background-image property.

From now on, I will use the following table example for all figures.

{% highlight html %}
<table>
  <tr><td>Hello World</td></tr>
  <tr><td>Hello World<br>Hello World</td></tr>
  <tr><td>Hello World</td></tr>
</table>
{% endhighlight %}
{% highlight css %}
td {
  font-size: 12px;
  line-height: 20px;
}
{% endhighlight %}

Example 1 shows a naïve example by adding 1px border on the bottom. Here, gridlines are rendered as red dots (24px), while table row borders are rendered as blue lines. We can see the discrepency between gridline and the row lines adds up.

{% highlight css %}
td {
  border-bottom: 1px solid rgba(0, 0, 255, 0.4);
}
{% endhighlight %}

<aside id='figure1'>
  <div class='figure-wrapper'>
    <div class='gridline'>
      <table>
        <tr><td>Hello World</td></tr>
        <tr><td>Hello World<br>Hello World</td></tr>
        <tr><td>Hello World</td></tr>
      </table>
    </div>
  </div>
  <figcaption>Example 1.</figcaption>
</aside>

Example 2 shows my next solution to make the sum of vertical padding and border to be the multiplication of the grid size. I distributed paddings on top and bottom evenly so the texts can lie in the middle of each row. It works, but it takes a lot of extra vertical spaces.

{% highlight css %}
td {
  padding-top: 10px;
  padding-bottom: 9px;
  border-bottom: 1px solid rgba(0, 0, 255, 0.4);
}
{% endhighlight %}

<aside id='figure2'>
  <div class='figure-wrapper'>
    <div class='gridline'>
      <table>
        <tr><td>Hello World</td></tr>
        <tr><td>Hello World<br>Hello World</td></tr>
        <tr><td>Hello World</td></tr>
      </table>
    </div>
  </div>
  <figcaption>Example 2.</figcaption>
</aside>

Since both solutions are unsatisfactory, I had been using striped tables instead of bordered table. But I recently came up with this solution using background-image property. Example 3 has table row borders perfectly aligned with the baselines.

{% highlight css %}
td {
  background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1' height='20'><rect x='0' y='19' width='1' height='1' fill='blue' fill-opacity='0.4'></rect></svg>");
  background-repeat: repeat-x;
  background-position: bottom;
}
{% endhighlight %}

<aside id='figure3'>
  <div class='figure-wrapper'>
    <div class='gridline'>
      <table>
        <tr><td>Hello World</td></tr>
        <tr><td>Hello World<br>Hello World</td></tr>
        <tr><td>Hello World</td></tr>
      </table>
    </div>
  </div>
  <figcaption>Example 3.</figcaption>
</aside>
