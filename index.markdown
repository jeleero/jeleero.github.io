---
layout: default
---
<section class="main-section">
  <div class="container">
  <h1>All Gift Ideas</h1>
  <p>All the gift ideas you could ever want for you husband, wife, mother, father or children they are all here so why not have a browse.</p>
    <div class="row row-cols-1 row-cols-lg-2 row-cols-xl-3">
      {% for post in site.posts %}
      <div class="col mb-4">
        <div class="card h-100">
          <p class="d-flex mx-auto card-image"> {{ post.affiliate-picture }} </p>
          <div class="card-body">
            <h2 class="card-title mb-0">{{ post.title }}</h2>
            <p class="card-text">{{ post.excerpt }}</p>
          </div>
          <div class="card-footer">
            <div class="d-flex align-items-end">
              <div class="card-footer-price-and-date">
                <p class="card-price">£{{ post.price }}</p>
                <p class="card-date">{{ post.date | date: "%Y-%m-%d" }}</p>
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