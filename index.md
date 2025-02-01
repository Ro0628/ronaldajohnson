## My Projects

{% for project in site.data.ds-projects %}
<div class="project-item">
    <h3><a href="{{ ds-project.repository_url }}" target="_blank">{{ ds-project.name }}</a></h3>
    <p>{{ ds-project.description }}</p>
    {% if ds-project.site_url %}
        <p><a href="{{ ds-project.site_url }}" target="_blank">Live Site</a></p>
    {% endif %}
    {% if project.image %}
        <img src="{{ ds-project.image }}" alt="{{ ds-project.name }}" width="200">
    {% endif %}
</div>
{% endfor %}

{% for project in site.data.gen-ai-projects %}
<div class="project-item">
    <h3><a href="{{ gen-ai-projects.repository_url }}" target="_blank">{{ gen-ai-projects.name }}</a></h3>
    <p>{{ gen-ai-projects.description }}</p>
    {% if project.site_url %}
        <p><a href="{{ gen-ai-projects.site_url }}" target="_blank">Live Site</a></p>
    {% endif %}
    {% if project.image %}
        <img src="{{ gen-ai-projects.image }}" alt="{{ gen-ai-projects.name }}" width="200">
    {% endif %}
</div>
{% endfor %}

<style>
    .project-item {
        border: 1px solid #ddd;
        padding: 10px;
        margin-bottom: 15px;
    }
</style>
