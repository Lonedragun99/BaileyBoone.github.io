# BaileyBoone.github.io
Class project
{% assign categories = page.categories %}
{% if categories.size > 0 %}
<div class="after-post-cats">
    <ul class="tags mb-4">
        <p>Categories:</p>
        {% assign sortedCategories = categories | sort %}
        {% for category in sortedCategories %}
        <li>
            <a class="smoothscroll" href="{{site.baseurl}}/categories#{{ category | replace: " "," -" }}">{{
                category }}</a>
        </li>
        {% endfor %}
    </ul>
</div>
{% endif %}

{% assign tags = page.tags %}
{% if tags.size > 0 %}
<div class="after-post-tags">
    <ul class="tags">
        <p>Tags:</p>
        {% assign sortedTags = tags | sort %}
        {% for tag in sortedTags %}
        <li>
            <a class="smoothscroll" href="{{site.baseurl}}/tags#{{ tag | replace: " "," -" }}">#{{ tag
                }}</a>
        </li>
        {% endfor %}
    </ul>
</div>
{% endif %}
