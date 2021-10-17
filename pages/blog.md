---
title: Jello App Coding Blog
nav: Blog
nav_order: 2
---


<div class="album py-5 bg-light">
    <div class="container">
        <div class="row">
            {% for post in site.posts %}
            <div class="col-md-4">
                <div class="card mb-4 box-shadow">
                    {%- comment -%} <img src="..." class="card-img-top" alt="..."> {%- endcomment -%}
                    <div class="card-body">
                        <h5 class="card-title">{{ post.title }}</h5>
                        <P>Author: <strong>{{ post.author }}</strong></P>
                        <P>{{ post.date| date_to_string }}</P>
                        <div>
                            <a href="{{ post.url }}" class="btn btn-sm btn-danger">See more</a>
                        </div>
                    </div>
                </div>
            </div>
            {% endfor %}
        </div>
    </div>
</div>



<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul style="list-style-type:none;">
    {% for post in tag[1] %}
      <h3><li><a class="text-decoration-none" href="{{ post.url }}">{{ post.title }}</a></li></h3>
      <P>{{ post.author }}</P>
      <P>{{ post.date| date_to_string }}</P>
    {% endfor %}
  </ul>
{% endfor %}

<div class="album py-5 bg-light">
    
    <div class="container">
        <div class="row">
            
            {% for tag in site.tags %}
            <div class="col-md-4">
                <div class="card mb-4 box-shadow">
                    
                    {% for post in tag[1] %}
                    {%- comment -%} <img src="..." class="card-img-top" alt="..."> {%- endcomment -%}
                    <div class="card-body">
                        <h5 class="card-title">{{ post.title }}</h5>
                        <P>Author: <strong>{{ post.author }}</strong></P>
                        <P>{{ post.date| date_to_string }}</P>
                        <div>
                            <a href="{{ post.url }}" class="btn btn-sm btn-danger">See more</a>
                            <strong class="float-right">{{ tag[0] }}</strong>
                        </div>
                    </div>
                    {% endfor %}
                </div>
            </div>
                {% endfor %}
    
    
        </div>
        
    </div>
</div>