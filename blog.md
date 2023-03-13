---
layout: main
title: Blog
---

<!-- ======= Portfolio Section ======= -->
<section id="blog" class="portfolio">
    <div class="container">
        <div class="section-title">
            <h2>Blog</h2>
            <p>
                Magnam dolores commodi suscipit. Necessitatibus eius consequatur ex aliquid fuga eum quidem. Sit sint consectetur velit. Quisquam quos quisquam cupiditate. Et nemo qui impedit suscipit alias ea. Quia fugiat sit in iste officiis commodi quidem hic quas.
            </p>
        </div>
        <div class="row" data-aos="fade-up">
            <div class="col-lg-12 d-flex justify-content-center">
                <ul id="portfolio-flters" style="background: #eee;">
                    <li data-filter="*" class="filter-active">All</li>
                    <li data-filter=".filter-academic">Academic</li>
                    <li data-filter=".filter-book">Book</li>
                    <li data-filter=".filter-business">Buiness</li>
                </ul>
            </div>
        </div>
        <div class="row">
        {% for post in site.posts %}
            <div class="col-lg-4 col-md-6 mb-2-6 .filter-{{ post.categories.first }}">
                <article class="card card-style2">
                    <div class="card-img">
                        <div class="fill hoverwrap">
                            <a class="image-wrapper image-zoom cboxElement" href="{{post.url}}">
                                <img src="{{post.img}}" class="rounded-top" alt="Photo of Blog">
                            </a>
                            <div class="hovercap">{{ post.title }}</div>
                        </div>
                        <div class="date"><span>{{ post.date | date: "%b" }}</span>{{ post.date | date: "%Y" }}</div>
                    </div>
                    <div class="card-body">
                        <h3 class="h4"><a href="{{post.url}}" title="{{ post.title }}">{{post.title | strip_html | truncate: 50}}</a></h3>
                        <p class="display-30">{{ post.brief | strip_html | truncate: 130 }}</p>
                        <a href="{{post.url}}" class="btn"><i class="fa fa-angle-double-right"></i> Read more</a>
                    </div>
                    <div class="card-footer">
                        <ul>
                            <li><i class="fa fa-user-circle-o"></i> {{ post.author }}</li>
                            <li><i class="fa fa-tags"></i> <span class="category"> {{ post.categories.first }} </span> </li>
                        </ul>
                    </div>
                </article>
            </div>
        {% endfor %}
        </div>
    </div>
</section><!-- End Portfolio Section -->