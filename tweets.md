---
layout: default
---

<h1>Tweets, Twetches, etc...</p></h1>

{% assign tweets = site.tweets | sort: 'date' | reverse %}
{% for tweets in tweets %}


 
 
<div class="tweet" style="margin-bottom:1em;">
  {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
   <time class="dt-published" style="display:inline;"datetime="{{ tweets.date | date_to_xmlschema }}" itemprop="datePublished">
        {{ tweets.date | date: date_to_rfc822 }}
 </time></a> {{ tweets.content | truncate: 445 }}</div>
 


 
   <!--{% if notes.image %}
      <div class="post-image">
        <a href="{{ notes.url | relative_url }}" style="
    text-decoration: none;
">
          <img src="{{ notes.image | relative_url }}" alt="{{ notes.alt }}">
          
        </a>
       </div>  
      {% endif %}-->
 

{% endfor %}  