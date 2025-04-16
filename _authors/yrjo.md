---
username: yrjo
name: Jorge Serrano
location: Madrid 🇪🇸
url_full: https://yrjo.eu/
url_short: yrjo.eu
bio: Soy un ferroviario que ama viajar, escribir, leer, hacer fotografías, cocinar, dibujar, y vivir nuevas aventuras y desafíos.
logo: /assets/img/avatar.jpg
email: yrjo@tuta.io
---

{% if page.picture %}
    <img class="author-profile-image" src="/{{ page.logo }}" alt="{{ page.name }}" />
{% endif %}
<h1 class="site-title">{{ page.name }}</h1>
{% if page.bio %}
    <h2 class="author-bio">{{ page.bio }}</h2>
{% endif %}
{% if page.location %}
    <div class="author-location">{{ page.location }}</div>
{% endif %}

{% for post in site.posts %}
	{% if post.authors contains page.username or page.username == post.authors %}
		<a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
	{% endif %}
{% endfor %}
