## My Projects

### Gen AI Projects
{% assign grouped_projects = site.data.gen_ai_projects | group_by: "type" %}
{% for group in grouped_projects %}
<h2 class="project-category">{{ group.name }}</h2>
<div class="projects-grid">
{% for project in group.items %}
<div class="project-item">
    <h3><a href="{{ project.repository_url }}" target="_blank">{{ project.name }}</a></h3>
    <p>{{ project.description }}</p>
    {% if project.site_url %}
        <p><a href="{{ project.site_url }}" target="_blank" class="live-site">Live Site</a></p>
    {% endif %}
    {% if project.image and project.image != "" %}
        <img src="{{ project.image }}" alt="{{ project.name }}" class="project-image">
    {% endif %}
</div>
{% endfor %}
</div>
{% endfor %}

### Machine Learning Projects
{% assign grouped_projects = site.data.ml_projects | group_by: "type" %}
{% for group in grouped_projects %}
<h2 class="project-category">{{ group.name }}</h2>
<div class="projects-grid">
{% for project in group.items %}
<div class="project-item">
    <h3><a href="{{ project.repository_url }}" target="_blank">{{ project.name }}</a></h3>
    <p>{{ project.description }}</p>
    {% if project.site_url %}
        <p><a href="{{ project.site_url }}" target="_blank" class="live-site">Live Site</a></p>
    {% endif %}
    {% if project.image and project.image != "" %}
        <img src="{{ project.image }}" alt="{{ project.name }}" class="project-image">
    {% endif %}
</div>
{% endfor %}
</div>
{% endfor %}

<style>
    body {
        font-family: 'Poppins', sans-serif;
        background: #fef6ff;
        color: #333;
    }
    .profile-section {
        text-align: center;
        padding: 30px;
    }
    .profile-pic {
        width: 150px;
        height: 150px;
        border-radius: 50%;
        border: 4px solid #ffb6c1;
        margin-bottom: 15px;
    }
    .name {
        font-size: 28px;
        color: #ff69b4;
    }
    .bio {
        max-width: 600px;
        margin: auto;
        font-size: 16px;
    }
    .linkedin-button {
        display: inline-block;
        padding: 10px 20px;
        background: #ff69b4;
        color: #fff;
        text-decoration: none;
        border-radius: 20px;
        margin-top: 10px;
    }
    .projects-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 20px;
        padding: 20px;
    }
    .project-category {
        font-size: 22px;
        color: #ff69b4;
        border-bottom: 2px solid #ffb6c1;
        padding-bottom: 5px;
        margin: 20px 0;
    }
    .project-item {
        background: white;
        border-radius: 10px;
        padding: 15px;
        text-align: center;
        box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s ease;
    }
    .project-item:hover {
        transform: scale(1.05);
    }
    .live-site {
        color: #ff69b4;
        font-weight: bold;
        text-decoration: none;
    }
    .project-image {
        max-width: 100%;
        border-radius: 8px;
        margin-top: 10px;
    }
</style>
