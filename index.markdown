---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Welcome!
layout: default
---

<!-- Jumbotron! -->
<div class="container col-xl-10 col-xxl-8 px-5 my-5 rounded-3 bg-body-tertiary">
  <div class="row align-items-center g-lg-5 py-5">
    <div class="col-lg-7 text-center text-lg-start">
      <h1 class="display-4 fw-bold lh-1 mb-3">Hello, world!</h1>
      <p class="col-lg-10 fs-4">Welcome to NASA Communities. A landing spot (and launchpad!) for employee and alumni clubs and such. Browse around and have a look!</p>
    </div>
    <div class="col-lg-5 text-center text-lg-start">
      <p class="text-muted"><em>We're a small team of volunteers that manage this site. If you'd like to get involved, come check out <a href="https://github.com/nasa-communities" target="_blank">our spot on GitHub <i class="fa-brands fa-github"></i></a></em></p>
    </div>
  </div>
</div>

<h1 class="pb-1 border-bottom">Clubs</h1>

<div class="row g-4 py-5 row-cols-1 row-cols-lg-4">
  {% for club in site.clubs %}
  <div class="feature col">
    <a href="{{ club.url }}" title="The {{ club.name }} Club!" class="link-underline-light">
      <div class="card text-bg-light h-100">
        <img src="/images/{{ club.thumbnail }}" class="card-img-top" alt="...">
        <div class="card-body">
          <h5 class="card-title">{{ club.name }}</h5>
          <p class="card-text">
            <em>{{ club.description }}</em>
          </p>
        </div>
        <div class="card-footer text-body-secondary">
          <em>{{ club.slogan }}</em>
        </div>
      </div>
    </a>
  </div>
  {% endfor %}
</div>