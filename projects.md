---
layout: default
title: Projects
---

<div class="project-grid">
    {% for item in site.projects %}
    <article class="project-card">
        {% if item.image %}
        <div class="card-image">
            <img src="{{ item.image }}" alt="{{ item.title }}">
        </div>
        {% endif %}
        <div class="card-content">
            <h2>{{ item.title }}</h2>
            <p>{{ item.description }}</p>
            {% if item.tags %}
            <div class="tags">
                {% for tag in item.tags %}
                <span class="tag">{{ tag }}</span>
                {% endfor %}
            </div>
            {% endif %}
            <a href="{{ item.url }}" class="read-more">View Details</a>
        </div>
    </article>
    {% endfor %}
</div>

<style>
.project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 2rem;
    padding: 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.project-card {
    background: white;
    border-radius: 0.5rem;
    overflow: hidden;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    transition: transform 0.2s, box-shadow 0.2s;
}

.project-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

.card-image {
    width: 100%;
    height: 200px;
    overflow: hidden;
}

.card-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.card-content {
    padding: 1.5rem;
}

.card-content h2 {
    margin: 0 0 1rem 0;
    font-size: 1.5rem;
}

.card-content p {
    color: #666;
    margin-bottom: 1rem;
    line-height: 1.5;
}

.tags {
    display: flex;
    gap: 0.5rem;
    flex-wrap: wrap;
    margin-bottom: 1rem;
}

.tag {
    background: #f0f0f0;
    padding: 0.25rem 0.75rem;
    border-radius: 1rem;
    font-size: 0.9rem;
    color: #666;
}

.read-more {
    display: inline-block;
    color: #007bff;
    text-decoration: none;
    font-weight: 500;
}

.read-more:hover {
    text-decoration: underline;
}
</style> 