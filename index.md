---
layout: index
---
<!-- Banner -->
<section id="banner">
    <div class="content">
        <header>
            <h1>Hi, I’m K</h1>
            <p>and I'm a Maker</p>
        </header>
        <p>Aenean ornare velit lacus, ac varius enim ullamcorper eu. Proin aliquam 		facilisis ante interdum congue.
            Integer mollis, nisl amet convallis, porttitor magna ullamcorper, amet egestas mauris. Ut magna finibus nisi
            nec lacinia. Nam maximus erat id euismod egestas. Pellentesque sapien ac quam. Lorem ipsum dolor sit nullam.
        </p>
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
				<h3>{{ post.title }}</h3>
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
