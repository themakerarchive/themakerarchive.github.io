---
layout: index
---
<!-- Banner -->
<section id="banner">
    <div class="content">
        <header>
            <h3>Hi, I’m Karen</h3>
            <p> I live in Dublin, Ireland</p>
<form style="border:1px solid #ccc;padding:3px;text-align:center;" action="https://tinyletter.com/themakerarchive" method="post" target="popupwindow" onsubmit="window.open('https://tinyletter.com/themakerarchive', 'popupwindow', 'scrollbars=yes,width=800,height=600');return true"><p><label for="tlemail">Enter your email address</label></p><p><input type="text" style="width:140px" name="email" id="tlemail" /></p><input type="hidden" value="1" name="embed"/><input type="submit" value="Subscribe" /><p><a href="https://tinyletter.com" target="_blank">powered by TinyLetter</a></p></form>
         
	</header>
    </div>
    <span class="image object">
        <img src="assets/images/themakerarchive-welcome.jpg" alt="" />
    </span>
</section>

<!-- Section -->
<section>
	<header class="major">
		<h2>Recent posts</h2>
	</header>
	<div class="posts">
		{% for post in site.posts limit:8 %}
			<article>
			    {% if post.image %}
					<a href="{{ post.url }}" class="image"><img src="{{ post.image | absolute_url }}" alt="" /></a>	
				{% endif %}

				<span class="postDate">{{ post.date | date: "%b %-d, %Y" }}</span>
				<h3>{{ post.title | upcase }}</h3>
				<p>{{ post.excerpt }}</p>
				<ul class="actions">
					<li><a href="{{ post.url }}" class="button">More</a></li>
				</ul>
			</article>
		{% endfor %}
	</div>
</section>

<p>
	<a class="icon fa-tags" href="{{ 'elements.html' | absolute_url }}"></a>
    {% for tag in site.tags %}
	<span>  |  </span>
    <a href="/tags/{{ tag[0] | slugify}}" 
    style="font-size: {{ tag[1] | size | times: 2 | plus: 10 }}px">{{ tag[0] }}</a>
    {% endfor %}
</p>
