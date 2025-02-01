## My Projects

### Gen AI Projects
{% assign grouped_projects = site.data.gen_ai_projects | group_by: "type" %}
{% for group in grouped_projects %}
### {{ group.name }}
{% for project in group.items %}
<div class="project-item">
    <h3><a href="{{ project.repository_url }}" target="_blank">{{ project.name }}</a></h3>
    <p>{{ project.description }}</p>
    {% if project.site_url %}
        <p><a href="{{ project.site_url }}" target="_blank">Live Site</a></p>
    {% endif %}
    {% if project.image %}
        <img src="{{ project.image }}" alt="{{ project.name }}" width="200">
    {% endif %}
</div>
{% endfor %}
{% endfor %}

### Machine Learning Projects
{% assign grouped_projects = site.data.ml_projects | group_by: "type" %}
{% for group in grouped_projects %}
### {{ group.name }}
{% for project in group.items %}
<div class="project-item">
    <h3><a href="{{ project.repository_url }}" target="_blank">{{ project.name }}</a></h3>
    <p>{{ project.description }}</p>
    {% if project.site_url %}
        <p><a href="{{ project.site_url }}" target="_blank">Live Site</a></p>
    {% endif %}
    {% if project.image %}
        <img src="{{ project.image }}" alt="{{ project.name }}" width="200">
    {% endif %}
</div>
{% endfor %}
{% endfor %}

<style>
    .project-item {
        border: 1px solid #ddd;
        padding: 10px;
        margin-bottom: 15px;
    }
</style>
