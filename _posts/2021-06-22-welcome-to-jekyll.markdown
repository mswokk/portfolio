---
layout: post
title:  "Welcome to Jekyll!"
date:   2021-06-22 10:18:04 +0900
categories: jekyll update
---

Hello

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:



{% highlight java linenos %}
@Override
public Completable writeRtc(LocalDateTime dateTime) {
  return createPacketTransceiver(CMD_WRITE_RTC)
    .putByte((byte) (dateTime.getYear() - 2000)) //2000 + year
    .putByte((byte) dateTime.getMonth().getValue())
    .putByte((byte) dateTime.getDayOfMonth())
    .putByte((byte) dateTime.getDayOfWeek().getValue())
    .putByte((byte) dateTime.getHour())
    .putByte((byte) dateTime.getMinute())
    .putByte((byte) dateTime.getSecond())
    .sendForAck();
}

{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
