---
layout: default
title: Test Collections
---

<div class="container">
    <section style="padding: 50px; background: white; margin: 40px 0;">
        <h2>Collection Test Page</h2>
        
        <h3>Team Collection:</h3>
        <p>Size: {{ site.team.size }}</p>
        <ul>
        {% for member in site.team %}
            <li>{{ member.name }}</li>
        {% endfor %}
        </ul>
        
        <h3>Publications Collection:</h3>
        <p>Size: {{ site.publications.size }}</p>
        <ul>
        {% for pub in site.publications %}
            <li>{{ pub.title }}</li>
        {% endfor %}
        </ul>
        
        <h3>All Collections:</h3>
        <ul>
        {% for collection in site.collections %}
            <li>{{ collection.label }}: {{ collection.docs.size }} items</li>
        {% endfor %}
        </ul>
    </section>
</div>