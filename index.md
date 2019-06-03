---
layout: index
---
<!-- Banner -->
<section id="banner">
    <div class="content">
        <header>
            <h1>Hi, I’m Karen</h1>
            <p> I live in Dublin, Ireland</p>
        </header>
        <p>This blog was originally created to share the things I learned in a silversmithing course last year, but isn’t it hard to portray only one facet of ourselves when we as individuals are agglomerations of our interests, life experiences, idiosyncrasies, etc.?</p>
		<p>As a place where the creative parts of myself collide, you can expect to read musings on jewellery, learn a thing or two about tea, and peak into the inner workings of my mind once in a while – with a lot of photos thrown in for good measure!</p>
		<p> Background: I am a woman of the tropics, though there is nothing quite as romantic to me as driving through the west coast on a misty day. My favourite colour is green – its mossy and emerald shades, a symbolic representation of the tropical jungles of the Philippines; the luscious Irish countryside after the rain. I’ve long accepted that my heart will always stand on a balance between these two shores, not favouring either, yet keeping myself open to what other cultures have to offer – all unique and beautiful in their own ways.</p>
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
