---
layout: default
title: News & Updates
---

<header>
    <div class="container">
        <h1>News & Updates</h1>
        <p>Latest developments from the NOME Lab</p>
    </div>
</header>

<div class="container">
    <section>
        <h2>Recent News</h2>
        
        {% for item in site.data.news %}
        <div style="background: white; padding: 30px; margin: 30px 0; border-left: 4px solid #18453B; border-radius: 5px; box-shadow: 0 2px 10px rgba(0,0,0,0.1);">
            <h3 style="color: #18453B; margin-bottom: 10px;">{{ item.title }}</h3>
            <p style="color: #666; font-size: 0.9em; margin-bottom: 15px;">{{ item.date }}</p>
            <p>{{ item.description }}</p>
        </div>
        {% endfor %}
        
        <div style="text-align: center; margin-top: 50px; padding: 40px; background: #f8f9fa; border-radius: 8px;">
            <p style="font-size: 1.1em;"><strong>Stay Updated!</strong></p>
            <p style="margin-top: 15px;">Follow our research progress and upcoming events.</p>
        </div>
    </section>
</div>