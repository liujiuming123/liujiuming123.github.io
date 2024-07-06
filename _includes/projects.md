## Projects

{% for project in site.data.projects %}
<div class="project">
  <h3 class="project-title">{{ project.title }}</h3>
  <p class="project-subtitle">{{ project.subtitle | markdownify }}</p>
  
  <div class="project-images">
    {% for image in project.images %}
    <div class="project-image">
      <img src="{{ site.baseurl }}/{{ image.src }}" alt="{{ image.alt }}">
      <div class="image-description">{{ image.description }}</div>
    </div>
    {% endfor %}
  </div>

  <p class="project-date">{{ project.date }}</p>
  
  <h4>Responsibilities:</h4>
  <ul class="project-responsibilities">
    {% for responsibility in project.responsibilities %}
    <li>{{ responsibility }}</li>
    {% endfor %}
  </ul>
  
  <p class="project-description">{{ project.description | markdownify }}</p>
  
  <div class="project-links">
    {% for link in project.links %}
    <a href="{{ link.url }}" target="_blank">{{ link.title }}</a>
    {% endfor %}
  </div>
</div>
{% endfor %}