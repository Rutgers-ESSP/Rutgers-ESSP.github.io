{% if author.home %}
### [ {{ author.name }} ]({{ author.home }})
{% else %}
### {{ author.name }}
{% endif %}

{% if author.avatar %}
![{{ author.name }}]({{ author.avatar }}){: style="float: right; margin:20px; max-width: 150px"}
{% endif %}

<div>
{{ author.longbio }}

{% if author.home %}
<a href="{{ author.home }}"><i class="fas fa-fw fa-home" aria-hidden="true"></i></a>
{% endif %}
{% if author.links %}
{% for link in author.links %}
{% if link.label and link.url %}
  <a href="{{ link.url }}" rel="nofollow noopener noreferrer"><i class="{{ link.icon | default: 'fas fa-link' }}" aria-hidden="true"></i></a>
{% endif %}
{% endfor %}
{% endif %}
{% if author.email %}
<a href="mailto:{{ author.email }}">
  <meta itemprop="email" content="{{ author.email }}" />
  <i class="fas fa-fw fa-envelope-square" aria-hidden="true"></i></a>
{% endif %}
{% if author.mastodon %}
<a href="{{ author.mastodon }}" itemprop="sameAs" rel="nofollow noopener noreferrer">
<i class="fab fa-fw fa-mastodon" aria-hidden="true"></i></a>
{% endif %}
{% if author.twitter %}
<a href="https://twitter.com/{{ author.twitter }}" itemprop="sameAs" rel="nofollow noopener noreferrer">
  <i class="fab fa-fw fa-twitter-square" aria-hidden="true"></i></a>
{% endif %}
{% if author.linkedin %}
<a href="https://www.linkedin.com/in/{{ author.linkedin }}" itemprop="sameAs" rel="nofollow noopener noreferrer">
  <i class="fab fa-fw fa-linkedin" aria-hidden="true"></i></a>
{% endif %}
{% if author.github %}
<a href="https://github.com/{{ author.github }}" itemprop="sameAs" rel="nofollow noopener noreferrer">
  <i class="fab fa-fw fa-github" aria-hidden="true"></i></a>
{% endif %}
{% if author.gitlab %}
<a href="https://gitlab.com/{{ author.gitlab }}" itemprop="sameAs" rel="nofollow noopener noreferrer">
  <i class="fab fa-fw fa-gitlab" aria-hidden="true"></i></a>
{% endif %}
{% if author.google.scholar %}
<a href="https://scholar.google.com/citations?user={{ author.google.scholar }}" itemprop="sameAs" rel="nofollow noopener noreferrer">
<i class="fab fa-google" aria-hidden="true"></i></a>
{% endif %}
{% if author.orcid %}
<a href="http://ORCID.org/{{ author.orcid }}" itemprop="sameAs" rel="nofollow noopener noreferrer">
<i class="fab fa-orcid" aria-hidden="true"></i></a>
{% endif %}
</div>


