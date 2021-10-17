---
title: Post
layout: default
---



<div class="album py-5 bg-light">
    <div class="container">
        <div class="row">
            <div class="col-md-12">
                    <div class="card-body">
                        <h1 class="card-title">{{ post.title }}</h1>
                        <P>Author: <strong>{{ post.author }}</strong></P>
                        <P>{{ post.date| date_to_string }}</P>
                        <div>
                            <a href="{{ post.url }}" class="btn btn-sm btn-danger">See more</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
</div>
