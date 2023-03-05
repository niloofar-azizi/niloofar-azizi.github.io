---
layout: main
title: Blog
---

<!-- ======= Portfolio Section ======= -->
<section id="blog" class="portfolio section-bg">
    <div class="container">
        <div class="section-title">
            <h2>Blog</h2>
            <p>Magnam dolores commodi suscipit. Necessitatibus eius consequatur ex aliquid fuga eum quidem. Sit sint consectetur velit. Quisquam quos quisquam cupiditate. Et nemo qui impedit suscipit alias ea. Quia fugiat sit in iste officiis commodi quidem hic quas.</p>
        </div>
        <div class="row" data-aos="fade-up">
            <div class="col-lg-12 d-flex justify-content-center">
            <ul id="portfolio-flters">
                <li data-filter="*" class="filter-active">All</li>
                <li data-filter=".filter-academic">Academic</li>
                <li data-filter=".filter-book">Book</li>
                <li data-filter=".filter-business">Buiness</li>
            </ul>
            </div>
        </div>
            <div class="row portfolio-container" data-aos="fade-up" data-aos-delay="100">
            {% for post in site.posts %}
                <div class="col-lg-4 col-md-6 portfolio-item filter-{{ post.categories.first }}">
                    <div class="portfolio-wrap">
                        <img src="{{ post.img }}" class="img-fluid" alt="{{ post.img }}">
                        <a href="{{ post.url }}">
                            <div class="portfolio-links">
                                <h3> {{ post.title }} </h3>
                            </div>
                        </a>
                    </div>
                </div>
            {% endfor %}
            </div>
    </div>
</section><!-- End Portfolio Section -->