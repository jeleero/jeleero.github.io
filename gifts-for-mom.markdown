---
layout: default
---
<section class="main-list">
<div class="container">
  <div class="row row-cols-1 row-cols-lg-2 row-cols-xl-3">
    {% assign filtered-posts = site.posts | where_exp:"item","item.categories contains 'gifts for mom'" %}
    {% for post in filtered-posts %}
    <div class="col mb-4">
      <div class="card h-100">
        <p class="d-flex mx-auto card-image"> {{ post.affiliate-picture }} </p>
        <div class="card-body">
          <h5 class="card-title">{{ post.title }}</h5>
          <p class="card-text">{{ post.excerpt }}</p>
        </div>
        <div class="card-footer">
          <div class="d-flex align-items-end">
          <div>
          <p class="post-date">£{{ post.price }}</p>
            <p class="post-date">{{ post.date | date: "%Y-%m-%d" }}</p>
          </div>
            <a href="#" class="btn btn-primary ml-auto"><i class="fab fa-facebook-square"></i></a>
            <a href="{{ post.afflitate-link }}" class="btn btn-primary ml-2">Go To Amazon</a>
          </div>         
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
</div>
</section>