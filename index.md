---
layout: default
title: Home
---

## My Projects

<script>
    fetch('projects.json')
        .then(response => response.json())
        .then(projects => {
            let projectContainer = document.getElementById('project-list');
            projectContainer.innerHTML = projects.map(project => `
                <div class="project-item">
                    <h3><a href="${project.repository_url}" target="_blank">${project.name}</a></h3>
                    <p>${project.description}</p>
                    ${project.site_url ? `<p><a href="${project.site_url}" target="_blank">Live Site</a></p>` : ''}
                    ${project.image ? `<img src="${project.image}" alt="${project.name}" width="200">` : ''}
                </div>
            `).join('');
        })
        .catch(error => console.error('Error loading projects:', error));
</script>

<div id="project-list"></div>

<style>
    .project-item {
        border: 1px solid #ddd;
        padding: 10px;
        margin-bottom: 15px;
    }
</style>
