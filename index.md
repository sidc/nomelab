---
layout: default
title: Home
---

<header>
    <div class="container">
        <h1>NOME Lab</h1>
        <p>Neuroscience of Meditation Lab</p>
        <div class="university">Michigan State University</div>
    </div>
</header>

<div class="container">
    <section id="about">
        <h2>About the Lab</h2>
        <p>The <strong>NOME Lab (Neuroscience of Meditation Lab)</strong> at Michigan State University advances the scientific understanding of meditation through data-driven research. We employ computational neuroscience, advanced signal processing, machine learning, and rigorous experimental psychology to study contemplative practices.</p>
        
        <p style="margin-top: 20px;">Our research focuses on quantifying neural dynamics during meditation using high-density EEG (64-channel wireless systems), spectral analysis (FOOOF decomposition, time-frequency representations), and multivariate classification methods. We investigate mantra-based meditation techniques through longitudinal studies, examining event-related potentials (P300), oscillatory biomarkers (alpha/theta power, IAF/IAP), and behavioral correlates (MAIA, FFMQ, PSS). Our goal is to establish evidence-based frameworks for meditation practice optimization through rigorous neuroscientific inquiry.</p>
        
        <p style="margin-top: 20px;"><strong>Leadership:</strong> The NOME Lab is directed by <strong>Dr. Saiprasad Ravishankar</strong> and has evolved from the <a href="https://slim-msu.github.io/" target="_blank">SLIM (Sensing, Learning, Imaging & Modeling) Lab</a>, expanding to focus specifically on contemplative neuroscience and meditation research.</p>
        
        <p style="margin-top: 20px;">We maintain an in-house EEGlab facility equipped with state-of-the-art 64-channel wireless EEG systems, enabling longitudinal studies that track neural changes over weeks and months of meditation practice.</p>
    </section>

    <section id="research">
        <h2>Research Areas</h2>
        <div class="research-areas">
            <div class="research-card">
                <h4>Exploring Neural Mechanisms and Effects of Contemplative Practices</h4>
                <p>Investigating the brain dynamics underlying various meditation techniques, including mantra-based practices (Hare Krishna, Sa Ta Na Ma) and breath-focused meditation. Using advanced spectral analysis, FOOOF decomposition, and machine learning to identify neural biomarkers and understand the transformative effects of sustained contemplative practice.</p>
            </div>
            
            <div class="research-card">
                <h4>Cognitive & Behavioral Changes</h4>
                <p>Examining longitudinal improvements in attention, cognitive processing speed (P300 latency), mindfulness, interoceptive awareness, and stress reduction through controlled meditation interventions lasting 6+ weeks. Understanding how consistent, deep practice leads to lasting neuroplastic changes and enhanced well-being.</p>
            </div>
            
            <div class="research-card">
                <h4>AI 4 Meditation State Detection</h4>
                <p>Using AI & machine learning for real-time meditation state classification. Applying our signal processing expertise to distinguish authentic meditative states from mind-wandering and rest.</p>
            </div>
        </div>

        <h3 style="margin-top: 50px;">Key Findings</h3>
        <ul style="margin-left: 30px; margin-top: 20px;">
            <li>Mantra-based meditation produces distinct alpha band modulations compared to breath-focused techniques</li>
            <li>Six weeks of daily practice significantly reduces P300 latency, indicating improved neural processing efficiency</li>
            <li>Meditation enhances interoceptive awareness (MAIA scores) across all technique types</li>
            <li>Individual Alpha Frequency (IAF) increases and Individual Alpha Power (IAP) decreases during meditation, suggesting enhanced attentional control</li>
            <li>Deep learning models with Stationary Wavelet Transform modules successfully classify meditation states with >90% accuracy</li>
            <li>Consistent deep practice is essential for accessing transformative meditative states</li>
        </ul>
    </section>

    <section id="gallery">
        <h2>📸 Gallery</h2>
        <p>Highlights from our lab activities, conference presentations, and research events.</p>
        
        <div class="gallery-grid">
            {% if site.data.gallery %}
                {% for item in site.data.gallery %}
                <div class="gallery-item" onclick="openLightbox('{{ item.image | relative_url }}')">
                    <img src="{{ item.image | relative_url }}" alt="{{ item.title }}">
                    <div class="gallery-caption">
                        <h4>{{ item.title }}</h4>
                        <p>{{ item.description }}</p>
                    </div>
                </div>
                {% endfor %}
            {% endif %}
        </div>
    </section>

<section id="team">
    <h2>Team</h2>
    
    <h3>Lab Members</h3>
    <div class="team-grid">
        {% assign lab_members = site.data.team | where: "category", "Lab Member" %}
        {% for member in lab_members %}
        <div class="team-member">
            <h4>{{ member.name }}</h4>
            <div class="role">{{ member.role }}</div>
            <p>{{ member.department }}</p>
        </div>
        {% endfor %}
    </div>

    <h3>Advisors</h3>
    <div class="team-grid">
        {% assign advisors = site.data.team | where: "category", "Advisor" %}
        {% for member in advisors %}
        <div class="team-member">
            <h4>{{ member.name }}</h4>
            <div class="role">{{ member.role }}</div>
            <p>{{ member.department }}</p>
        </div>
        {% endfor %}
    </div>

    <p style="margin-top: 30px;"><em>We also gratefully acknowledge our expert meditation instructors Devin O'Rourke (Harmony Collective, Ypsilanti), and our dedicated data collectors including Pratham Pradhan, Annie Wozniak, Vu Song Thuy Nguyen, Wei-ting Tan, Alisia Coipel, and Genevieve Orlewicz.</em></p>
</section>

    <section id="publications">
        <h2>Selected Publications</h2>
        <ul class="publications">
            {% assign sorted_pubs = site.data.publications | sort: 'year' | reverse %}
            {% for pub in sorted_pubs %}
            <li>
                <strong>{{ pub.authors }}</strong> ({{ pub.year }}). "{{ pub.title }}" <em>{{ pub.venue }}.</em>
                {% if pub.pdf %}
                <br><a href="{{ pub.pdf | relative_url }}" target="_blank">📄 View Poster (PDF)</a>
                {% endif %}
                {% if pub.link and pub.link != "" %}
                <br><a href="{{ pub.link }}" target="_blank">🔗 Link</a>
                {% endif %}
            </li>
            {% endfor %}
        </ul>
        <p style="margin-top: 30px;"><em>Additional research supported by Brainwave Science, Inc. and collaborations across partner institutions.</em></p>
    </section>

    <div class="opportunities">
        <h2 style="color: #ff6600; border-color: #ff6600;">🎓 Join Our Lab</h2>
        
        <div class="opportunity-box">
            <h3>PhD Student Positions Available</h3>
            <p><strong>We are actively seeking motivated PhD students</strong> to join the NOME Lab. Ideal candidates will have:</p>
            <ul style="margin: 15px 0 15px 30px;">
                <li>Background in neuroscience, computational science, biomedical engineering, psychology, or related fields</li>
                <li>Strong interest in meditation research and contemplative neuroscience</li>
                <li>Experience with signal processing, machine learning, or EEG analysis (preferred but not required)</li>
                <li>Strong programming skills (Python, MATLAB)</li>
            </ul>
            <p><strong>What we offer:</strong> Opportunities to work on cutting-edge meditation studies, publish in top-tier journals, and contribute to understanding how to optimize meditation practice.</p>
            <a href="mailto:{{ site.email }}" class="btn btn-secondary">Apply for PhD Position</a>
        </div>

        <div class="opportunity-box">
            <h3>Summer Research Internships</h3>
            <p><strong>Undergraduate and Master's students</strong> are invited to apply for summer research internships.</p>
            <ul style="margin: 15px 0 15px 30px;">
                <li>Gain hands-on experience with EEG data collection and analysis</li>
                <li>Learn advanced signal processing and machine learning techniques</li>
                <li>Contribute to ongoing meditation neuroscience studies</li>
                <li>Co-author research publications and conference presentations</li>
            </ul>
            <p><strong>Duration:</strong> 8-12 weeks | Remote or In-person<br>
            <strong>Eligibility:</strong> Current undergraduate or Master's students in relevant fields</p>
            <a href="mailto:{{ site.email }}" class="btn btn-secondary">Apply for Summer Internship</a>
        </div>
    </div>

    <section id="contact">
        <h2>Contact Us</h2>
        <div class="contact-info">
            <p><strong>For PhD positions, internships, or collaboration inquiries:</strong></p>
            <p>Email: <a href="mailto:{{ site.email }}">{{ site.email }}</a></p>
            <p><strong>Lab Director:</strong><br>
            Dr. Saiprasad Ravishankar<br>
            Department of Computational Mathematics, Science and Engineering<br>
            Michigan State University<br>
            East Lansing, MI 48824</p>
        </div>
    </section>
</div>

<!-- Lightbox Modal -->
<div id="lightbox" class="lightbox" onclick="closeLightbox()">
    <span class="lightbox-close">&times;</span>
    <img class="lightbox-content" id="lightbox-img">
</div>